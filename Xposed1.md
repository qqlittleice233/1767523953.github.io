# Xposed (1)

### 1. Create App Project

#### Create No Activity Project
![image](https://user-images.githubusercontent.com/60041789/135718475-27da15d7-ed25-4b8d-aa30-f6b41c191d03.png)

#### Edit Your Project Information
![image](https://user-images.githubusercontent.com/60041789/135718563-f4ca08e4-4e00-4a60-b4a7-287e548b183d.png)

#### Add Dependence
![image](https://user-images.githubusercontent.com/60041789/135718692-020303b5-1e05-4551-86f1-7ca8dc17faa2.png)
![image](https://user-images.githubusercontent.com/60041789/135718728-ee228d69-e20b-452f-87d8-3f9fbaae8772.png)

#### Declare this is a xposed module (Only for Lsposed)
![image](https://user-images.githubusercontent.com/60041789/135718821-31c6f9f6-c512-486a-bdec-8a88f77e149a.png)
##### Before: 
![image](https://user-images.githubusercontent.com/60041789/135718995-a722e7ae-75ec-4cff-97b3-f0480b7a5ec7.png)
##### After: 
![image](https://user-images.githubusercontent.com/60041789/135718975-02828677-4e7c-4e0c-9cc1-d146228517ec.png)

#### Create MainHook.kt
![image](https://user-images.githubusercontent.com/60041789/135719568-ecbfcad2-e46c-40d7-a8cb-83738337ba1f.png)
##### Implement IXposedHookLoadPackage and Override handleLoadPackage
![image](https://user-images.githubusercontent.com/60041789/135719651-e52746f3-0e8c-4ff8-8347-a4a810559c8a.png)

### I make a test app that you can hook it easier - [download](https://github.com/1767523953/1767523953.github.io/raw/master/TestApp1.apk)
![Screenshot_2021-10-02-22-11-23-865_hk qqlittleice](https://user-images.githubusercontent.com/60041789/135720068-3b54e4ab-59ee-4800-b39b-2bc5c1248f2b.jpg)
### We will hook the text which in the centre

#### Check the smali
![image](https://user-images.githubusercontent.com/60041789/135720154-29f1698c-5fb6-4de3-822e-7774fe92fa9f.png)
##### We only need to hook this method's result

#### Write Code for Hook
![image](https://user-images.githubusercontent.com/60041789/135720457-357f8995-a657-4d72-8e34-065ddef25b56.png)

#### Declare The Entry for Lsposed
##### Create Assets Folder
![image](https://user-images.githubusercontent.com/60041789/135720531-c73fa4ea-702b-4f78-9442-8576d2714fef.png)
##### Create xposed_init File
![image](https://user-images.githubusercontent.com/60041789/135720564-f74e2957-486f-421d-aecf-5d1b30ce8329.png)
##### Content In xposed_init (should be your entry's class path)
![image](https://user-images.githubusercontent.com/60041789/135720582-014b1cb5-902a-4685-91aa-189d0637dc6f.png)

#### Finally, Build and Install and Active
![Screenshot_2021-10-02-22-26-22-035_org lsposed ma](https://user-images.githubusercontent.com/60041789/135720776-384da0b8-6208-48a4-b0c0-b84438cbf4dd.jpg)
##### Result:
![Screenshot_2021-10-02-22-26-41-053_hk qqlittleice](https://user-images.githubusercontent.com/60041789/135720805-dd769aaa-c77e-4592-8352-0711df620e0d.jpg)

