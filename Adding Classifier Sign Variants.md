## Folder Structure

> Cluster
> > Type
> > > Country
> > > > Variant 

Adding a new sign variant should only include specifying Type and Country.
Possible ways to add new signs:
- Batch script in _Cluster_/_Type_/_Country_ e. g. *add_sign_variant_drop_file.bat* 
	- Drag and drop a PNG file of any size on this .bat file.
	- PNG file will be automatically resized and renamed too e. g. `US_02.png`, where 02 is the first available variant number.
- ...