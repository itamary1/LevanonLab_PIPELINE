# LevanonLab_PIPELINE


If you not run on levanon labs servers, you need to take care of the following:

    download/create all the following genomic files and set teh following params:
        # genome fasta
        params.genome_file
        # expression_file like "ucscHg38GTExGeneExpression.bed.gz"
        params.expression_file 
        # star indexd genome
        params.star_genome
        # refSeq genes file like ucscHg38RefSeqCurated.bed.gz
        params.refseq_file
        # snps file like ucscHg38CommonGenomicSNPs150.bed.gz
        params.snp_file
        # salmon transcripts index
        params.transcripts_index
        # for salmon - like gencode_v32.transcriptToGeneID.tab
        params.tx2id_geneMap 

    take care of code that not run inside dockers:
        You can disable the summarizing scripts with the params
        run_cmp_summarize = false
        run_salmon_summary = false
        run_star_summarize_script = false

        If you run the summarize scripts, you need python2.7 with the packeges:
        os
        argparse
        sys
        subprocess
        traceback
        
        set 'which_python_27' to your python interpreter
        
        You also need to have and R running with 'Rscript' command with the following libraries:
        argparse
        cowplot
        data.table
        dplyr
        ggplot2
        log4r
        purrr
        reshape2
        tibble
        tidyr
