# L03: The Training Lifecycle

## Overview

This lesson traces the full lifecycle of training a large language model, from pre-training on massive internet-scale datasets through supervised fine-tuning and alignment. You will understand how knowledge cutoffs arise, what fine-tuning changes about a model, and why training decisions affect the models you use in production.

## Topics Covered

- Pre-training: learning from internet-scale data
- Data collection, filtering, and deduplication at scale
- Supervised fine-tuning (SFT) with curated datasets
- Reinforcement learning from human feedback (RLHF) and alignment
- Knowledge cutoffs: what models know and when they stop knowing
- The difference between pre-training knowledge and fine-tuned behavior
- Implications of training choices for downstream application developers

## Key Takeaways

- Pre-training creates broad world knowledge; fine-tuning shapes behavior and instruction-following
- Knowledge cutoffs mean models have a fixed snapshot of world knowledge that does not update automatically
- RLHF alignment training is what makes models helpful, harmless, and honest
- Understanding the training lifecycle helps you predict what a model can and cannot do
- Fine-tuning changes how a model responds, not fundamentally what it knows
