Functions to transform Seurat object to Scanpy object

### Citation
SOAPy

### Tutorial
Download the source file Seurat2Scanpy.py and import the functions:  
exec(open('Seurat2Scanpy.py','r').read())  
r_home="/home/lijiarong/miniconda3/envs/R/lib/R" # path of R console with Seurat installed
For scRNA-Seq data:  
adata=sc_Seurat2Scanpy('seurat_obj.rds',r_home,
                    exp_mat_slot=['RNA','data'])
For 10X Visium data:  
adata=st_Seurat2Scanpy('seurat_obj.rds',r_home,
                    exp_mat_slot=['RNA','data'],res_type='lowres')

