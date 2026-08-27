## Hey, I'm Carmit

DevOps and AI infrastructure engineer. I'm the sole DevOps for a biotech startup - AWS end to end, Terraform across three environments, an ISO 27001 posture, and an HPC migration to bare metal that cut cost by ~87%. On the AI side I build and measure: distributed training on H100s, LLM serving under SLOs, agents with real evaluation suites. I also train DevOps engineers - 60+ so far - and wrote the AI-engineering syllabus my company delivers today.

Every repo here ships with a README written for the next engineer, and where there are numbers, CI re-derives them from committed logs.

**Live:** [Causa](https://causa.develeap.com) - an AI incident-investigation agent I designed and built at Develeap: tiered L0-L3 architecture, ~$0.04 per investigation, a 123-case scored eval suite.

**What I Work With**

`Terraform` `AWS` `Kubernetes` `EKS` `Nebius mk8s` `ArgoCD` `Helm` `GitHub Actions` `Jenkins` `Prometheus` `Grafana` `Python` `PyTorch` `DDP/NCCL` `vLLM` `SkyPilot` `MLflow` `Airflow` `LangGraph`

### AI infrastructure - Nebius Academy, AI Performance Engineering (2026)

- **[ddp-scaling-anatomy](https://github.com/CarmitHaas/ddp-scaling-anatomy)** - GPT-2 Large with PyTorch DDP on 1 vs 4 H100 nodes (Nebius mk8s + SkyPilot). Every NCCL all-reduce timed: communication is 100% of a 15x step slowdown over TCP; inference scaled 3.80x. CI re-derives every number from the logs.
- **[text-to-sql-vllm-slo](https://github.com/CarmitHaas/text-to-sql-vllm-slo-carmit-haas)** - LangGraph text-to-SQL agent on Qwen3-30B FP8 (vLLM, H100) with Prometheus/Grafana/Langfuse and an SLO load test. The diagnosis: TTFT 200 ms vs P95 108 s - the bottleneck was agent shape, not GPU.
- **[customer-service-agent](https://github.com/CarmitHaas/customer-service-agent-carmit-haas)** - LangGraph ReAct agent over the Bitext dataset: router-first graph, Pydantic tools, persistent memory plus a per-user profile, tools shared with a FastMCP server.
- **[coding-agent-eval-pipeline](https://github.com/CarmitHaas/coding-agent-eval-pipeline)** - Airflow DAG with MLflow tracking for evaluating coding agents on SWE-bench Verified; one comparable row per run, durable artifacts, best batch 8/15 bugs resolved.
- **[agentic-ai-playbook](https://github.com/CarmitHaas/agentic-ai-playbook)** - my working notebook of the techniques and mistakes behind building LLM agents, kept current as I build.
- [multinode-ddp-skypilot](https://github.com/CarmitHaas/multinode-ddp-skypilot) - two-node DDP on Nebius managed Kubernetes via SkyPilot, NCCL rendezvous captured in the logs.
- [roofline-to-cuda-graphs](https://github.com/CarmitHaas/roofline-to-cuda-graphs) - GPU kernel profiling to the roofline on H100, then CUDA graphs.
- [quant-serving-bf16-vs-fp8](https://github.com/CarmitHaas/quant-serving-bf16-vs-fp8) - vLLM serving benchmarked BF16 vs FP8 against latency SLOs.
- [eval-driven-development](https://github.com/CarmitHaas/eval-driven-development) - LLM-as-judge evaluation pipeline with human baselines and judge-agreement analysis.

### Platform and DevOps

- **[HA-infrastructure](https://github.com/CarmitHaas/HA-infrastructure)** - Terraform EKS with custom modules: VPC, managed node groups, ArgoCD, EBS CSI, secrets via AWS Secrets Manager.
- **[gitops-HA](https://github.com/CarmitHaas/gitops-HA)** - ArgoCD app-of-apps, Helm umbrella chart, Prometheus/Grafana, EFK logging, cert-manager, SealedSecrets.
- **[Horsing Around](https://github.com/CarmitHaas/Horsing-Around)** - the full path end to end: Flask app, Jenkins CI/CD, EKS, ArgoCD GitOps, Prometheus and EFK.
- [repo-summarizer](https://github.com/CarmitHaas/repo-summarizer) - FastAPI + multi-LLM GitHub repository analyzer.
- **[Docker Learning Path](https://github.com/CarmitHaas?tab=repositories&q=docker)** - progressive Docker and Compose exercises with hints and solution branches, built for the engineers I train.

### Certifications

<a href="https://www.credly.com/badges/301eca18-df18-4683-898c-df7f8a82b09e/public_url"><img src="https://images.credly.com/size/100x100/images/4c15a070-84b8-4951-bc4f-95adeea32f9a/blob" alt="Nebius Academy - AI Performance Engineering Fellowship" title="Nebius Academy: AI Performance Engineering – Fellowship (2026)" /></a>&nbsp;
<a href="https://www.credly.com/badges/824202aa-660d-4e62-a13d-f817ce958be6/public_url"><img src="https://images.credly.com/size/100x100/images/0e284c3f-5164-4b21-8660-0d84737941bc/image.png" alt="AWS Solutions Architect Associate" title="AWS Certified Solutions Architect – Associate" /></a>&nbsp;
<a href="https://www.credly.com/badges/9066c488-8e46-4ba3-9cb5-8d97c7f42ccc/public_url"><img src="https://images.credly.com/size/100x100/images/0dc62494-dc94-469a-83af-e35309f27356/blob" alt="Terraform Associate" title="HashiCorp Certified: Terraform Associate (003)" /></a>&nbsp;
<a href="https://www.credly.com/badges/6db65302-72fe-4a01-8f90-c0e39918af4a/public_url"><img src="https://images.credly.com/size/100x100/images/7d2c6621-0b7f-46e6-a56b-f69143812011/blob" alt="GitOps Enterprise" title="GitOps Enterprise – Codefresh" /></a>&nbsp;
<a href="https://www.credly.com/badges/f55808b5-9589-498e-bc5a-c4f0357f20fb/public_url"><img src="https://images.credly.com/size/100x100/images/89046afe-b82b-4dc1-9c20-384ea505fd01/blob" alt="GitOps at Scale" title="GitOps at Scale – Codefresh" /></a>&nbsp;
<a href="https://www.credly.com/badges/57fd53e8-ac26-4607-8980-2ac89ade3157/public_url"><img src="https://images.credly.com/size/100x100/images/fbd71e9c-07f7-4a8b-a874-2bf5001a6dbf/blob" alt="GitOps Fundamentals" title="GitOps Fundamentals – Codefresh" /></a>&nbsp;
<a href="https://learn.microsoft.com/en-us/users/carmithaas-8969/credentials/certification/github-foundations"><img src="https://images.credly.com/size/100x100/images/024d0122-724d-4c5a-bd83-cfe3c4b7a073/image.png" alt="GitHub Foundations" title="GitHub Foundations" /></a>&nbsp;
<a href="https://learn.microsoft.com/en-us/users/carmithaas-8969/credentials/certification/github-actions"><img src="https://images.credly.com/size/100x100/images/89efc3e7-842b-4790-b09b-9ea5efc71ec3/image.png" alt="GitHub Actions" title="GitHub Actions" /></a>&nbsp;
<a href="https://learn.microsoft.com/en-us/users/carmithaas-8969/credentials/certification/github-copilot"><img src="https://images.credly.com/size/100x100/images/6b924fae-3cd7-4233-b012-97413c62c85d/blob" alt="GitHub Copilot" title="GitHub Copilot" /></a>&nbsp;

**Nebius Academy course badges** - each maps to the repos in the AI infrastructure section above

<a href="https://www.credly.com/badges/0ac70638-0dfa-4532-967e-765672a18316/public_url"><img src="https://images.credly.com/size/80x80/images/09cf81f7-74aa-42a4-8858-d7f1cdb944f6/blob" alt="AI Agents" title="Nebius Academy: AI Agents – Course Passed" /></a>&nbsp;
<a href="https://www.credly.com/badges/c62d0575-c13f-4756-8c07-963d8e06c2b1/public_url"><img src="https://images.credly.com/size/80x80/images/2c13b954-b97e-4ccd-98a5-0d515410555b/blob" alt="LLM Architectures" title="Nebius Academy: LLM Architectures – Course Passed" /></a>&nbsp;
<a href="https://www.credly.com/badges/5671e781-e651-441d-a2b6-86733fb3fb71/public_url"><img src="https://images.credly.com/size/80x80/images/b0680f98-9d73-4a7e-82a7-632e97767b8a/blob" alt="MLOps" title="Nebius Academy: MLOps – Course Passed" /></a>&nbsp;
<a href="https://www.credly.com/badges/671cc50d-9dd1-48c2-8f08-41feb19a6ded/public_url"><img src="https://images.credly.com/size/80x80/images/d5f20b27-4ae3-4a43-a8e6-c446af47f0e9/blob" alt="Performance Engineering" title="Nebius Academy: Performance Engineering – Course Passed" /></a>&nbsp;
<a href="https://www.credly.com/badges/2a95db7a-8b5b-4400-9519-628fe93d0cba/public_url"><img src="https://images.credly.com/size/80x80/images/d40c8569-3c8f-494b-86f8-01931d0e906d/blob" alt="LLM Post-Training" title="Nebius Academy: LLM Post-Training – Course Passed" /></a>&nbsp;

### How I teach

I design exercises where you learn by breaking things and fixing them. The Docker exercises above are battle-tested with real students - progressive difficulty, collapsible hints for when you're stuck, and solutions you can check after you've tried. The same rule runs through the AI repos: real measurements, the failure modes named, written so the next engineer can reproduce them.

### Connect

[LinkedIn](https://www.linkedin.com/in/carmit-shemesh-haas) · carmithaas@gmail.com
