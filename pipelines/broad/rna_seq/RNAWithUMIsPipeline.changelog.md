# 1.0.2
2022-02-18 (Date of Last Commit)

* Updated the STAR command line arguments, as follows:
    * Add "--alignEndsProtrude 20 ConcordantPair"; to rescue the case where the insert size drops below the read length and the sequencer starts to read into the adapters.
    * Removed "--limitSjdbInsertNsj 1200000"; the default of 1,000,000 is sufficient.
    * Removed "--outSAMstrandField intronMotif", defaults to "None"
* Slightly reduced memory and disk usage on several tasks.
* Standardized memory sizing.

# 1.0.1
2022-02-01 (Date of Last Commit)

* Updated SortSam task to be able to use call caching.
* Updated STAR aligner to 2.7.10a for RNAWithUMIs pipeline.
* Addressed memory usage in CheckFingerprint task to allow sufficient headroom for the VM.

# 1.0.0
2022-01-14 (Date of Last Commit)

* Initial Release of RNAWithUMIs pipeline.
* The RNA with UMIs pipeline is an open-source, cloud-optimized workflow created for processing total RNA isolated with the Transcriptome Capture (TCap) method, but can be used to process any bullk RNA-seq data. Overall, the workflow performs UMI correction, aligns reads to the genome, quantifies gene counts, and calculates quality metrics to produces genome- and transcriptome-aligned BAMs, BAIs, and a merged quality metrics file.

