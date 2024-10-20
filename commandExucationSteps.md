1. cd membership_inference
    download dataset: bash download_and_extract.sh

2. cd CodeGPT/dataset/py150/
    i. Configure load_py150.py
        - line 88: change base_dir = "{/home/mhaque4/Desktop/MIA}/membership_inference/py150_files"
                                      replace the contents of {} with your path (absolute path), remove {}

        - line 89: change output dir = "{/home/mhaque4/Desktop/MIA}/membership_inference/inference"
                                        replace the contents of {} with your path (absolute path), remove {}
    ii. Configure util.py
        - line 8: change output dir = "{/home/mhaque4/Desktop/MIA}/membership_inference/CodeGPT/dataset/py150/literals.json"
                                        replace the contents of {} with your path (absolute path), remove {}
    iii. Run
            python load_py150.py
    iv. (optional) If you want to change other hyperparameters (nshdow = 10, ntrain = 24000, neval = 2000), change from the lines 90,91,92.

3.

