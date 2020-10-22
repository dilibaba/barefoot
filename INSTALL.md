Ubuntu 18.04+ 安装说明

## 安装PostgreSQL + PostGIS (10.0版本)
```shell script
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo apt install postgis
```

## 安装依赖python库 (仅支持python2.7)
```shell script
sudo apt install python-psycopg2 python-numpy python-gdal
```

## 安装osmosis
osmosis用于将osm格式的路网数据导入PostgreSQL <br>
仓库链接: https://github.com/openstreetmap/osmosis
```shell script
cd ~/Downloads
wget https://github.com/openstreetmap/osmosis/releases/download/0.48.3/osmosis-0.48.3.zip
mkdir "osmosis"
unzip -d osmosis osmosis-0.48.3.zip
sudo mv osmosis /usr/local
echo "export PATH=${PATH}:/usr/local/osmosis/bin" >> ~/.bashrc
```

