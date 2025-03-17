## Upscale Drone Processing: RGB and Multispectral Imagery Processing in Agisoft Metashape Pro

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
  - [Automated Processing Workflow](#automated-processing-workflow)
  - [Step-by-Step Processing Using the Metashape GUI](#step-by-step-processing-using-the-metashape-gui)
  - [Other Examples](#other-examples)
- [Funding](#funding)
- [Authors](#authors)
- [Acknowledgements](#acknowledgements)
- [Contributing](#contributing)

## Introduction
These workflows were developed for RGB and multispectral imagery collected simultaneously on the DJI Matrice 300 platform. These scripts are designed for use with RGB imagery acquired with DJI Zenmuse P1 and MicaSense RedEdge-MX/Dual.

**Note:** The images are expected to be loaded into the Metashape project already, and the projects are created by the `CreateMultispectralProjects` and `CreateUpscaleProjects` scripts.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/JajjusZiegler/Upscale_Drone_Processing.git
   ```
2. Install required dependencies:
   ```bash
   cd Upscale_Drone_Processing
   pip install -r requirements.txt
   ```

## Usage

### Automated Processing Workflow
Uses scripts `RunScript.py`, `UpscaleProcessing.py` , `upd_micasense_pos.py` and `CreatUpscaleProjects.py`. 
- Run `CreatUpscaleProjects.py` to create Metashape projects with a CSV input file.
- Place `OpenProjectsfromCSV.py` in the `C:\Program Files\Agisoft\Metashape Pro\scripts` folder. Open Metahape and run the script Select Project from CSV. Select the reflectance Panel images and detect the panel masks. Click on a new project to open the next project.
- Run `RunScript.py`to complete the processing workflow.
- Inspect the output.

### Step-by-Step Processing Using the Metashape GUI


### Running the UpscaleProcessing Script
To run the `UpscaleProcessing` script:
1. Ensure all dependencies are installed (refer to the Installation section).
2. Navigate to the directory containing the script.
3. Execute the script with the required arguments. For example:
   ```bash
   python UpscaleProcessing.py -proj_path <path_to_project_file> -date <YYYYMMDD> -site <site_name> -crs <EPSG_code>
   ```

### Other Examples
- `examples/metashape_blockshift.py`: Code to perform the block shift of images in a Metashape chunk using AUSPOS results.
- `examples/metashape_proc_p1.py`: Process RGB images captured using Zenmuse P1 on **gimbal 1 of dual mount**. **Remove the GPS/INS offset code if P1 was on single mount gimbal.**

## Funding
This project was funded by TERN Landscapes.

## Authors
- Poornima Sivanandam (Original Author)
- Darren Turner (Original Author)
- Arko Lucieer (Original Author), School of Geography, Planning, and Spatial Sciences, University of Tasmania
- Jan Ziegler (Modifying Author)

## Acknowledgements
- TERN Landscapes
- TERN Surveillance
- TERN Data Services

## Contributing
Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests.
