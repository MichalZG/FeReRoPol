# savartPhot

Software for data analysis of Suhora Telescope with Savart Plates polarimetry system

## Prerequisites

* 64-bit linux
* Python 3 (Anaconda package strongly recommended)

## Installation
### 1. Clone this respository
```
git clone https://github.com/MichalZG/savartPhot.git
```
### 2. Create anaconda environment
```
conda create --name savart --file spec-file.txt
```
## Running
### Depending on the way you want to use it:  

* Create links to programs for using like bash programs:
```
sudo ln -s <path_to_run_scrip>t /usr/bin/<name>
sudo chmod +x /usr/bin/<name>
```

OR  

* Use jupyter run_example.ipynb notebook
```
jupyter-notebook run_example.ipynb
```

OR

* Use like normal python scripts

run list  
```
python run_list_objects.py <path_to_config_file> <path_to_data>
```
run stack
```
python run_stack.py <path_to_config_file> <path_to_data> <stack_number> <path_to_output>  
```
run photometry  
```
python run_savart_phot.py <path_to_config_file> <path_to_stack_output> <path_to_star_coordinate_file> <path_to_output>
```

Important note:  
photometry need coordinate file of stars, where y1 > y2 !  
```
P1 x1 y1 x2 y2  - Star coordinates from reference P1 savart image
P3 x1 y1 x2 y2  - Star coordinates from reference P3 savart image
```
example:  
```
P1 544 256 450 245  
P3 566 354 477 344  
```



