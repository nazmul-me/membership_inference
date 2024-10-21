1. Browse to the directory
    ```shell
        cd membership_inference
    ```
    download dataset: 
    ```shell
    bash download_and_extract.sh
    ```

2. Data split and preprocess: Browse to the directory
    ```shell
        cd CodeGPT/dataset/py150/
    ```
    i. Configure load_py150.py
    ```shell
    - line 88: change base_dir = "{/home/mhaque4/Desktop/MIA}/membership_inference/py150_files"
    ```
    replace the contents of {} with your path (absolute path), remove {}

    ```shell
    - line 89: change output dir = "{/home/mhaque4/Desktop/MIA}/membership_inference/inference"
    ```
    replace the contents of {} with your path (absolute path), remove {}

    ii. Configure util.py
    ```shell
    - line 8: change output dir = "{/home/mhaque4/Desktop/MIA}/membership_inference/CodeGPT/dataset/py150/literals.json"
    ```
    replace the contents of {} with your path (absolute path), remove {}

    iii. Run
    ```shell
    python3 load_py150.py
    ```
    iv. (optional) If you want to change other hyperparameters ```(nshdow = 10, ntrain = 24000, neval = 2000)```, change from the ```lines 90,91,92```.

3. Model Training: Browse to the directory
    ```shell
        cd CodeGPT/code/
    ```
    You need to change ```model = "shadow_{0-9}"``` if you have 10 shadow models and ```dir_prefix``` with your working directory. Other hyperparameters are to be changed based on the needs. Then run the following
    ```shell
    python3 run_lm.py
    ```
4. 

