常用命令

```
1. check conda version
conda --version = conda -V

2. check and modify config
conda config --show
conda config --show channels
conda config --add channels conda-forge
conda config --remove channels channel_name
```



创建删除复制环境：

```
1. create
conda create -n env_name python==3.9

2. clone create
conda create --name new_env_name --clone old_env_name

3. switch 
conda activate deeplearning 
conda activate | conda deactivate

4. check 
conda env list 
conda info -e 
conda info --envs（*当前环境)

5. del 
conda remove --name env_name --all 
conda remove --name env_name  package_name（删除环境中的某些包）
```



包管理

```
1. search
conda search cudatoolkit -c  conda-forge

2. download
conda install cudatoolkit==11.2.0 -c conda-forge

3. check
conda list
conda list pkgname 
conda list pkgname*

4. update
conda update pkgname 

5. uninstall
conda uninstall pkg_name
```







