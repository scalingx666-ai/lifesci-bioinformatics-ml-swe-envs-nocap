# Build notes - Bioinformatics & ML for Biology

Repo2RLEnv pr_diff (v0.9.6), Harbor-format output. Domain: bioinformatics-ml.

## Funnel

| Stage | Count |
|---|---|
| Domain candidates (deduped) | 399 |
| After active+star+noise filter | 228 |
| Final target list (cap unlimited) | 228 |
| Repos with >=1 task | 6 |
| Repos with 0 tasks | 93 |
| Total tasks (unlimited (no per-repo cap)) | 240 |

## Generation

- Shared task bank: each repo generated once (pr_diff, limit=3,
  max_files_per_pr=15, min_loc_changed=2), 4-way concurrency,
  rate-limit-aware with .done checkpoint resume.
- Per-domain consolidation: rank by reward_calibration.loc_changed desc,
  keep ALL qualifying tasks (no per-repo cap). Zero-yield repos are NOT fabricated.
- Overlap with the 3 published cancer editions is allowed (user decision);
  domains are independent selections, not a partition of one repo set.

## Zero-yield repos (informational, 93)

- kska32/ebooks
- speedyapply/2027-AI-College-Jobs
- beamandrew/medical-data
- google/highway
- spark-notebook/spark-notebook
- openworm/OpenWorm
- Biohub/esm
- zhaoyang97/Paper-Notes
- marcomusy/vedo
- dmis-lab/biobert
- SheffieldML/GPy
- bytedance/Protenix
- stephenturner/oneliners
- timsainb/noisereduce
- rust-bio/rust-bio
- myshell-ai/AIlice
- xianshang33/llm-paper-daily
- mdipierro/nlib
- NVIDIA-NeMo/Gym
- opensim-org/opensim-core
- scverse/anndata
- scverse/PyDESeq2
- zaeleus/noodles
- oschwengers/bakta
- fritzsedlazeck/Sniffles
- datavzrd/datavzrd
- rrwick/Bandage
- gamcil/clinker
- chapmanb/bcbb
- ysig/GraKeL
- nf-core/sarek
- biod/sambamba
- Martinsos/edlib
- tseemann/snippy
- marcelm/cutadapt
- ialbert/biostar-central
- jorvis/biocode
- plotly/dash-bio
- lindenb/jvarkit
- biogo/biogo
- bowang-lab/BioReason
- gao-lab/Guideline-for-Computational-Biology-and-Bioinformatics
- reneshbedre/bioinfokit
- daler/pybedtools
- brewsci/homebrew-bio
- wurmlab/sequenceserver
- lynnlangit/gcp-for-bioinformatics
- ugeneunipro/ugene
- biowasm/biowasm
- mothur/mothur
- ucscGenomeBrowser/kent
- linsalrob/ComputationalGenomicsManual
- OpenChemistry/avogadroapp
- ANHIG/IMGTHLA
- kyclark/biofx_python
- gladstone-institutes/Bioinformatics-Workshops
- PecanProject/pecan
- aquaskyline/SOAPdenovo2
- ssadedin/bpipe
- StaPH-B/docker-builds
- westlake-repl/ProTrek
- stjude-rust-labs/sprocket
- PacktPublishing/Bioinformatics-with-Python-Cookbook-third-edition
- ISUgenomics/bioinformatics-workbook
- biodatageeks/polars-bio
- ArcInstitute/SRAgent
- wheretrue/biobear
- lynnlangit/aws-for-bioinformatics
- MrOlm/inStrain
- ENCODE-DCC/kentUtils
- briscverse/ryp
- VerisimilitudeX/DNAnalyzer
- art-egorov/lovis4u
- westlake-repl/SaprotHub
- aquaskyline/Clairvoyante
- pengzhangzhi/faplm
- MGI-tech-bioinformatics/DNBelab_C_Series_HT_scRNA-analysis-software
- harvardinformatics/bioinformatics-coffee-hour
- hgbrian/biomodals
- burkesquires/python_biologist
- rcedgar/usearch12
- QizhiPei/BioT5
- THUDM/ProteinLM
- BojarLab/glycowork
- YosefLab/Cassiopeia
- ISYSLAB-HUST/ProtFlash
- chanzuckerberg/czid-web
- earmingol/cell2cell
- montilab/hypeR
- servierhub/top-pharma50
- labstructbioinf/pLM-BLAST
- elttaes/Revisiting-PLMs
- oxpig/CaLM

## Caveats

- Static validation only; real grading needs an LLM judge key + Docker.
- inline_dockerfile mode skips image build (no Docker daemon needed to publish).
- Provider secrets in upstream diffs were redacted before public release.
