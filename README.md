# EvoPoli-installation
Here it is described the process to install EvoPoli in Eclipse IDE, a tool that supports synthesis of Pareto-optimal policies for MDPs with arbitrary combinations of constraints and optimisation objectives.  https://eprints.whiterose.ac.uk/178508/1/MDPPolicySynthesis_ASE2021.pdf 


# Installation
 - Dowload and unzip the source code from: https://github.com/gerasimou/MDPSynthesis
 - Open Eclipse in a desire workingspace
 - Go to File Menu> Import > Maven > Existing Maven Projects and click next
 
 ![image](https://user-images.githubusercontent.com/63869574/139691001-89a4987a-fd80-44b9-9511-c90e052cfcf7.png)

- In the Root Directory, select the unzipped folder. It contains the pom.xml file which is automatically uploaded in the Projects box. Add project to the working set, and Finish.
![image](https://user-images.githubusercontent.com/63869574/139691902-1a22ad13-bbcb-477d-88e4-0a6a7175cb88.png)

- When finish importing, must probably the next Errors will appear:
![image](https://user-images.githubusercontent.com/63869574/139692068-6daca272-9493-4f89-870a-f9717e2328af.png)


- Go to Run> Run Configurations> Double click Maven Build. In the new configuration, in "Base dicrectory" select the Maven Project.
![image](https://user-images.githubusercontent.com/63869574/139694266-b37e02df-1d01-4c43-a08c-c1de91a41454.png)

- In the Environment tab> Add (for linux):
![image](https://user-images.githubusercontent.com/63869574/139694660-3d695f9c-7d82-4450-9e86-d5778599358f.png)
 or OSX: DYLD_LIBRARY_PATH = libs/runtime for Mac iOS.
 Apply and close.

- In the pom.xml, we can see that there are dependencies that are not uploaded yet:
![image](https://user-images.githubusercontent.com/63869574/139695456-447a95a2-5dba-4e2b-84a1-b7b065018c0a.png)
Hence, right click on the project folder > Maven > Add Dependency
![image](https://user-images.githubusercontent.com/63869574/139695662-d787d954-bc20-46f4-bbcf-3812593290a1.png)



- 


- Right click on the Project in the File's tree > Build Path > Configure Build Path
![image](https://user-images.githubusercontent.com/63869574/139692292-8878a479-905f-4c5b-b13b-e872705a4fe3.png)

- 
