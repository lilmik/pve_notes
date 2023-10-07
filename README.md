# pve_notes
pve使用相关命令

### .img.gz解压命令
```bash
gunzip ./<file_name>.img.gz

```

### .img转.qcow2命令
```bash
qemu-img convert -f raw -O qcow2 <file_name>.img <output_diskname>.qcow2
```

### .qcow2导入命令
```bash
qm importdisk <vmid> <images-name> <storage pool>  --format=<disk-fs> 
vmid：vm的id 例如102
images-name：磁盘镜像的名字
storage pool: 存储磁盘镜像的位置，如lvm-thin local
disk-fs: 磁盘镜像格式  raw/vmdk/qcow2
```

### 旁路由配置
```bash
nano /etc/config/network
```
