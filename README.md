# EvoPoli-installation
Here it is described the process to install EvoPoli in Eclipse IDE, a tool that supports synthesis of Pareto-optimal policies for MDPs with arbitrary combinations of constraints and optimisation objectives.  https://eprints.whiterose.ac.uk/178508/1/MDPPolicySynthesis_ASE2021.pdf 


## Installation
 - Dowload and unzip the source code from: https://github.com/gerasimou/MDPSynthesis
 - Open Eclipse in a desire workingspace
 - Go to File Menu> Import > Maven > Existing Maven Projects and click next
 
 ![image](https://user-images.githubusercontent.com/63869574/139691001-89a4987a-fd80-44b9-9511-c90e052cfcf7.png)

- In the Root Directory, select the unzipped folder. It contains the pom.xml file which is automatically uploaded in the Projects box. Add project to the working set, and Finish.
![image](https://user-images.githubusercontent.com/63869574/139691902-1a22ad13-bbcb-477d-88e4-0a6a7175cb88.png)

- When finish importing, must probably the next Errors will appear:
![image](https://user-images.githubusercontent.com/63869574/139692068-6daca272-9493-4f89-870a-f9717e2328af.png)

- Right click on the project folder > Import. Under Maven select:
![image](https://user-images.githubusercontent.com/63869574/139838441-929001cf-7789-4e1a-b63f-9c0eea70e591.png)

In "Artifact file", browse for the EvoChecker-1.1.0.jar that comes in the unzipped folder. In my case: /home/evochecker/Downloads/MDPSynthesis-master/EvoChecker-1.1.0.jar
Complete the group ID, artefact ID and version as it appears on the pom.xl file, and the rest as shown here:

![image](https://user-images.githubusercontent.com/63869574/139839694-c51da31d-783c-491a-a21e-f4941093caf9.png)

- Right click on the project folder again and press Refresh (F5)
![image](https://user-images.githubusercontent.com/63869574/139841260-7c797075-df73-4983-bdfe-a054c7aefb80.png)

The error for the Evochecker library should have dissapeared.
![image](https://user-images.githubusercontent.com/63869574/139841361-06918bbb-28d1-450a-8f7c-523a5224b71e.png)

- Extract Evochecker in the project folder
![image](https://user-images.githubusercontent.com/63869574/139842070-4f8da4b6-2c83-4f2d-9a10-ed97a1185b96.png)

- Go to https://automata.tools/hoa/jhoafparser/ and download the jhoafparser-xxx.jar
![image](https://user-images.githubusercontent.com/63869574/139846429-decb724d-6930-49ca-bf04-24a37fa1fa45.png)

- Repeate the process (as for Evochecker) to install the new artifact.
![image](https://user-images.githubusercontent.com/63869574/139846811-050b99ac-fd04-4a95-8c74-913fccc515a5.png)

In this case, I changed later the version in the pom.xml to match the .jar version "1.1.1"
![image](https://user-images.githubusercontent.com/63869574/139846965-16c9a65c-3f58-42dc-819d-fc0cfe4b18f7.png)
Save the new pom.xml, and refresh.*

Now there are three errors missing:
![image](https://user-images.githubusercontent.com/63869574/139847319-4c6bf53b-255b-49f9-b703-555b6e1514b8.png)

- Go to https://sourceforge.net/projects/lpsolve/files/lpsolve/5.0.10.0/ (FYI, mentionated in https://www.prismmodelchecker.org/papers/fmsd-csgs.pdf) and download lpsolve 
and download: lp_solve_5.0_java.zip
![image](https://user-images.githubusercontent.com/63869574/139855126-82110408-92f2-4c66-9592-15e0d6dd8790.png)

- Repeat process (as for Evochecker) to install the new artifact.
![image](https://user-images.githubusercontent.com/63869574/139855509-e1f75f84-62ea-4226-ba78-434df3e113e2.png)
Change to the downloaded version:
![image](https://user-images.githubusercontent.com/63869574/139855600-b1d02d40-f707-4f5c-806d-d9152cde8fa4.png)
Save the new pom.xml, and refresh.*
The pom.xml file should not have more errors.

## 

Error related to importing these libraries may exist:
![image](https://user-images.githubusercontent.com/63869574/139873599-17544c00-5542-412f-8402-385ac44b404d.png)




## Notes
* Sometimes Eclipse may require to Clean the project (Project > Clean) or to restart Eclipse to consider changes.


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
