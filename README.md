# sparc-ardell-workflow
A MAP Client workflow for the Ardell Heart Registration.

This workflow is created with the goal of matching electrical data to video data to analyse the ecltromechanical coupling.

## Walkthrough

### Tracking fidcucial points
![Selecting Fiducials](https://user-images.githubusercontent.com/37255664/57826211-5dbf7780-77f6-11e9-8dc5-89ca7710f22e.png)

### Fitting the heart scaffold to the fiducial points
![Scaffold Fitting](https://user-images.githubusercontent.com/37255664/57826242-8c3d5280-77f6-11e9-93be-638085fd16f9.png)

### Tracking the electrodes in image
![Electrode Tracking](https://user-images.githubusercontent.com/37255664/57826261-aecf6b80-77f6-11e9-82fb-f438a8fcf771.png)

### Projecting electrodes onto the surface of the heart
![MAPClient - images-flow 16_05_2019 4_15_41 PM](https://user-images.githubusercontent.com/37255664/57826288-c6a6ef80-77f6-11e9-8ddd-5b1bab541a9c.png)

### Registering the electrical data onto the mesh
![MAPClient - ecg-testing 16_05_2019 4_18_22 PM](https://user-images.githubusercontent.com/37255664/57826315-df170a00-77f6-11e9-89c9-ceb1ba804807.png)

## Installation

1. Install the following directories in the 'plugins' folder of mapclient:

```
git clone https://github.com/mahyar-osn/mapclientplugins.imagecontextdatamaker.git
git clone https://github.com/mahyar-osn/mapclientplugins.imagebasedfiducialmarkers.git
git clone https://github.com/mahyar-osn/mapclientplugins.parametricfittingstep.git
git clone https://github.com/mahyar-osn/mapclientplugins.electrodearraydetectorstep.git
git clone https://github.com/mahyar-osn/mapclientplugins.electrodeprojectionstep.git 
git clone https://github.com/hsorby/mapclientplugins.ecgstep.git
```

2. Install opencmiss zinc:
download the SDK, add to PATH and then
`pip install -e ~\OpenCMISS Libraries SDK\lib\python3.6\Release\opencmiss.zinc`

3. Install opencmiss.zinc.utils
git clone https://github.com/hsorby/opencmiss.utils.git
then move opencmiss.utils.zinc to the working directory

(or maybe `pip install git+https://github.com/hsorby/ZincPythonTools.git` will work?)

5. More dependencies:
```
pip install git+https://github.com/hsorby/PySideX.git
pip install git+https://github.com/mahyar-osn/sparc.electrodeprojection.git
pip install git+https://github.com/mahyar-osn/sparc.parametricfitting.git
pip install git+https://github.com/mahyar-osn/heart-video-tracking
```

(if these pip install don't work just clone and add to working directory path)

6. Go to this commit of imagecontext data maker
```
cd mapclientplugins.imagecontextdatamaker
git checkout d5606d4a8caaadb8529b6ff1c733f05b7851eb59
```




