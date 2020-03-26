# Python项目标准化操作



## 创建虚拟环境

virtualenv是跨平台的，linux、mac、windows都可以使用。  
  


> \#安装  
> pip install virtualenv  
> \#使用  
> virtualenv 目录  
>  \#激活环境  
> source 目录/bin/activate

### 生成依赖

  
使用 pipreqs 这个工具的好处是可以通过对项目目录的扫描，自动发现使用了那些类库，自动生成依赖清单。有可能会有些偏差。  
  


> \#安装  
> pip install pipreqs  
> \# 使用  
> pipreqs ./

### 安装依赖

> pip install  -r requirements.txt

