Checkpointing enables the training of deep learning models under restricted
memory budgets by freeing intermediate activations from memory and recomputing
them on demand. Current checkpointing techniques statically plan these
recomputations offline and assume static computation graphs. We demonstrate
that a simple online algorithm can achieve comparable performance by
introducing Dynamic Tensor Rematerialization (DTR), a greedy online algorithm
for checkpointing that is extensible and general, is parameterized by eviction
policy, and supports dynamic models. We prove that DTR can train an N-layer
linear feedforward network on an Ω(√ N) memory budget with only O(N) tensor
operations. DTR closely matches the performance of optimal static checkpointing
in simulated experiments. We incorporate a DTR prototype into PyTorch merely by
interposing on tensor allocations and operator calls and collecting lightweight
metadata on tensors.
