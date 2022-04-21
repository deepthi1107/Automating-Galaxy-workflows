# Automating-Galaxy-workflow
## Following the below steps helps in acheiveing the automated Galaxy workflow

`git clone https://github.com/usegalaxy-eu/workflow-automation-tutorial.git`

`cd workflow-automation-tutorial`

`ls`

**Python installation of Planemo**

`python3 -m venv planemo`

`. planemo/bin/activate`

`pip install planemo`

**Upgrading planemo**

`. planemo/bin/activate`

`pip install -U planemo`

**After installation follow the below steps**

`cd example`

`ls`

`planemo workflow_job_init tutorial.ga -o tutorial-init-job.yml`

`cat tutorial-init-job.yml`

`printf "hello\nworld" > dataset1.txt`

`printf "hello\nuniverse!" > dataset2.txt`

`ls`

`planemo run tutorial.ga tutorial-init-job.yml --galaxy_url <SERVER_URL> --galaxy_user_key <YOUR_API_KEY> --history_name "Test Planemo WF" --tags "planemo-tutorial"`

`planemo run tutorial.ga tutorial-init-job.yml --galaxy_url <SERVER_URL> --galaxy_user_key <YOUR_API_KEY> --history_name "Test Planemo WF with no_wait" --tags "planemo-tutorial" --no_wait`

`planemo run <WORKFLOW ID> tutorial-init-job.yml --galaxy_url <SERVER_URL> --galaxy_user_key <YOUR_API_KEY> --history_name "Test Planemo WF with Planemo" --tags "planemo-tutorial" --no_wait`

`planemo profile_create planemo-tutorial --galaxy_url <SERVER_URL> --galaxy_user_key <YOUR_API_KEY>`

`planemo run <WORKFLOW ID> tutorial-init-job.yml --profile planemo-tutorial --history_name "Test Planemo WF with profile" --tags "planemo-tutorial"`

**Automated Workflows**

`cd ../pangolin`

`ls`

`planemo workflow_job_init vcf2lineage.ga -o vcf2lineage-job.yml`

`cat vcf2lineage-job.yml`

`Create "create_job_file.py"`

`planemo run vcf2lineage.ga vcf2lineage-job.yml --profile planemo-tutorial --history_name "vcf2lineage test"`

`bash run_vcf2lineage.sh`

**Below are the results of the above commands**

[Test Planemo WF](https://usegalaxy.eu/u/deepthi_m/h/test-planemo-wf)

[Test Planemo WF 1](https://usegalaxy.eu/u/deepthi_m/h/test-planemo-wf-1)

[vcf2lineage test](https://usegalaxy.eu/u/deepthi_m/h/vcf2lineage-test)

[CWL Target History 1](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history-1)

[CWL Target History 2](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history-2)

[CWL Target History 3](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history-3)

[CWL Target History 4](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history-4)

[CWL Target History 5](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history-5)

[CWL Target History 6](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history-6)

[CWL Target History 7](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history-7)

[CWL Target History 8](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history-8)

[CWL Target History 9](https://usegalaxy.eu/u/deepthi_m/h/cwl-target-history)





