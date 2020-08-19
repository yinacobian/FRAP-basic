# FRAP-basic

#get FRAP-basic

git clone https://github.com/yinacobian/FRAP-basic.git

cd FRAP-basic

#make database directory

mkdir DB

cd DB

cp /home/SHARE/ViromicsWorkshop/reference-Nitrogen/NitrogenBacteria.fasta .

cd ..

#make datasets directory

mkdir DS

cd DS

cp /home/acobian/viromics/reads/subsample* .

cd ..

#run FRAP

perl jmf4.pl /home/acobian/viromics/FRAP-basic/DB/NitrogenBacteria.fasta /home/acobian/viromics/FRAP-basic/DS /home/acobian/viromics/FRAP-basic/results smalt 50000

#jmf4.pl [path to fasta file that would be the database] [path to datasets containing folder] [path to results directory that would be created] [mapper to be used: smalt or hisat2] [average genome length to use]
