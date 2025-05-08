# Sex_Check

 My sex-check folder is: /gpfs/gibbs/project/olfson/srg52/Project_3_Emily/Target/Quality Control/Quality Control of Related and Sex/Family_Factors/Gender_Check. 

Files you need: 
-Binary plink files (bed, bim, and fam) 
-plink1.9 
-pedigree 

1. Request a compute node in the terminal:  
       salloc -t 2:00:00 --mem=8G

2. Write the following in the terminal: 
       module load PLINK/1.9b_6.21-x86_64
3. Write in terminal: plink --bfile FINAL_OCD --check-sex
NOTE: replace FINAL_OCD with your plink binary file name

4. The output will contain a file with your sample ids and their SNP sex(Ignore status, this is because we didn't insert a pedigree).

5. Run Gender_Analysis_Correct.R to identify if mom and dad are correct
