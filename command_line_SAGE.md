# trimming script

        #!/bin/bash

#SBATCH --job-name malick_trimming
#SBATCH --partition normal
#SBATCH --time 20:00
#SBATCH --mem 12G
#SBATCH --nodes 1   #you use one server (=node)
#SBATCH --ntasks 1
#SBATCH --cpus-per-task 8 #in the server you use 8 pc's per task
#SBATCH --error trimmo_error #where do i put my errors
#SBATCH --output trimmo_output


module add UHTS/Analysis/trimmomatic/0.36
trimmomatic PE -threads 8 24_S23_L001_R1_001.fastq.gz 24_S23_L001_R2_001.fastq.$

