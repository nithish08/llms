Output approximation methods - 
1. Quantization
    - can be applied as inference only operation
    - Quantization aware training (QAT)

2. Distillation
    - Teacher and student model


Output preserving methods

1. Flash Attention
    - self dot-production attention is quadratic operation in input length
    - flash attention - optimizes the attention by making attention IO Aware. minimizes the data movement between HBM (high bandwidth memory) and faster memory tier (SRAM/VMEM) in TPUs or GPUs. when calculation attention order of operations is changed and multiple layers are fused so that we can utilize the faster memory tiers as efficienty as possible.

2. Prefix caching
    - cache the previous inputs from users during conversation for faster access to the K

3. Speculative Decoding
    - Speculative decoding uses a smaller, faster "drafter" model to predict tokens ahead of the main model, allowing parallel verification of hypotheses by the main model, which significantly reduces latency without compromising quality.
    - For effective speculative decoding, alignment between the drafter and main model is crucial to ensure token predictions are accepted, making quality training of the drafter model important for optimal performance.
    - Yes, verification is faster than generation in speculative decoding. The smaller drafter model quickly generates token predictions ahead of the main model, and the main model then verifies these predictions in parallel rather than generating tokens from scratch for each step. This parallel verification uses the extra compute capacity, speeding up the process while ensuring quality.

