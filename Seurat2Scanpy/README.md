Functions to transform Seurat object to Scanpy object

### Citation
SOAPy

### Tutorial
1. To use the script here, you should prepare an R console with `Seurat`, `SeuratObject`  
2. Sample `.rds` files of ST datasets could be downloaded from  
3. Download the source file Seurat2Scanpy.py and import the functions:  
```
exec(open('Seurat2Scanpy.py','r').read())  
r_home="/home/lijiarong/miniconda3/envs/R/lib/R" # path of R console 
```
3. For scRNA-Seq data:  
```
adata=sc_Seurat2Scanpy('seurat_obj.rds',r_home,
                    exp_mat_slot=['RNA','data'])
```
4. For spatial-omics data:  
```
adata=st_Seurat2Scanpy('seurat_obj.rds',r_home,
                    exp_mat_slot=['RNA','data'],res_type='lowres')
```
`exp_mat_slot` is a list with `assay` and `slot` name of expression matrix in seurat object to export to `adata.X`.