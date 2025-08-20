# HR Interview Video — Script (Danil Kazancev)

_Last updated: August 20, 2025_

---

## Q1) Have I deployed models in high-traffic production environments?
Yes. I’ve led deployments for **photo and video moderation** and for **video generation** at scale.  
- At **Wildberries**, I shipped a moderation system that served around **100 million users** with full autoscaling, monitoring, and incident response.  
- At **GLAM**, I productionized a video-generation service used by **about 10 million users**, designed with strict latency and reliability goals.  
- At **Mayflower (Lovescape)**, I rolled out image and video generation for **around 30 million users**, handling **about 30,000 requests per day**.  

In all of these, I was responsible for model training and optimization, inference tuning, GPU planning, Docker/K8s rollouts, observability, and on-call operations.

---

## Q2) Do I have experience with video generation workflows and models?
Yes. I currently run a **custom image-to-video pipeline in production** that produces **1K-resolution clips in about 40 seconds** on modern GPUs.  

The system uses diffusion backbones optimized with temporal consistency, attention and kernel tweaks, caching, and safe prompt conditioning. I’ve also worked on 2K pipelines, but the current setup balances **quality, speed, and cost** for real-world product use.

---

## Q3) Am I comfortable working with uncensored models and reviewing content for safety?
Yes. At **Wildberries**, I regularly reviewed uncensored inputs and outputs for **safety and quality assurance**. I follow strict access controls, reviewer well-being practices, and escalation paths. The focus is always on preventing risky content — never promoting it.

---

## Q4) Do I have trained LoRAs for video generation?
Yes. I’ve trained LoRAs for **all the current image-to-video actions** we use in production. This improves style control, identity consistency, and frame-to-frame stability. I apply low-precision training, gradient checkpointing, and curated negatives to stabilize temporal behavior.

---

## Q5) What type of contract do I prefer?
I prefer **B2B** since I’m fully set up for it, but I’m also open to **EOR** if that works better for the company’s operations.

---

## Q6) Am I comfortable with NSFW content?
Yes, as long as it’s **legal and policy-compliant**. My focus is always on **moderation, safety, and evaluation**. I minimize unnecessary exposure, automate checks wherever possible, and keep all activity auditable.

---

## Q7) Do I have other offers or ongoing recruitment processes?
I’m **not actively applying**, but I am **selectively exploring a few inbound conversations** — usually two or three at a time. I don’t have signed offers right now. My priority is finding strong product fit and impact.

---

## Q8) How do I monitor model training performance, and what metrics do I use?
For generative models, I look at **CLIP score, FID, KID, LPIPS**, and for video, **FVD** and temporal consistency. I also do human evaluations and track safety pass rates.  

For moderation models, I track **precision, recall, F1**, and especially **false negatives by class**.  

Operationally, I monitor **latency, throughput, VRAM usage, cost per sample**, and data drift with alerts. Together, these metrics keep both quality and reliability on track.

---

## Q9) Which frameworks and tools do I use for training? Am I more UI- or code-oriented?
I’m primarily **code-oriented**. I use **PyTorch**, **Hugging Face diffusers and transformers**, and sometimes Triton. For serving, I use **FastAPI, Docker, and Kubernetes**.  

I do prototype with **ComfyUI or Automatic1111** when it speeds iteration, but production systems are always scripted, version-controlled, and CI/CD driven.

---

## Q10) How do I prevent risky content from leaking into models?
I use a **defense-in-depth** approach:  
- During data curation, I apply blocklists, perceptual hashes, ML filters, and age/identity checks.  
- During training, I use curated negatives, safe conditioning, and prompt filters.  
- After generation, I run detectors for NSFW and underage content, deepfake checks, and metadata verification.  

Finally, everything is backed by policy-aligned eval sets, red-teaming, and audit logs. The goal is both **user trust and legal compliance**.

---

## Q11) What are my salary expectations?
For **B2B contracts**, I target **USD 10,000 net per month**.  
For **EOR employment**, I’d look for a gross base that nets to around the same — typically about **USD 140K to 160K annually**, depending on jurisdiction. I’m also open to discussing equity or bonus structures depending on scope and impact.

---

## Q12) How actively am I recruiting or applying?
I’m **not actively applying**. Most conversations come from **recruiter outreach**, and I’m selective about which ones I pursue. I focus on teams working on **video generation, LoRA customization, and content safety at production scale**, since that’s where I add the most value.

---
