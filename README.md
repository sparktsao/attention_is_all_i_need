# attention_is_all_i_need

python -m venv .venv
pip install torch torchvision torchaudio --pre --index-url https://download.pytorch.org/whl/nightly/cpu

(.venv) sparkt@US-SPARKT-M3 attention_is_all_i_need % python main.py 
[Transformer] src.shape: torch.Size([16, 7]), trg.shape: torch.Size([16, 7])
[make_src_mask] mask.shape: torch.Size([16, 1, 1, 7])
[make_trg_mask] mask.shape: torch.Size([16, 1, 7, 7])
[TransformerEncoder] Input x.shape: torch.Size([16, 7])
[TransformerEncoder] After word embedding x.shape: torch.Size([16, 7, 40])
[PositionalEncoding] Input x.shape: torch.Size([16, 7, 40]), Adding positional encodings for sequence length and embedding size.
[PositionalEncoding] Output shape: torch.Size([16, 7, 40])
[TransformerEncoder] Processing layer 1
[TransformerBlock] Starting block processing. Input dimensions - value: torch.Size([16, 7, 40]), key: torch.Size([16, 7, 40]), query: torch.Size([16, 7, 40])
[MultiHeadAttention:1] Input shapes (V, K, Q) - values: torch.Size([16, 7, 40]), keys: torch.Size([16, 7, 40]), queries: torch.Size([16, 7, 40])
[MultiHeadAttention:2] After linear projections V/K/Q multihead- values: torch.Size([16, 7, 4, 10]), keys: torch.Size([16, 7, 4, 10]), queries: torch.Size([16, 7, 4, 10])
[MultiHeadAttention:3] Energy = Q * K (raw attention scores) shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:4] Applying mask with shape: torch.Size([16, 1, 1, 7])
[MultiHeadAttention:5] Attention SoftMax weights shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:6] Attention * V = Output shape after weighted sum: torch.Size([16, 7, 40])
[TransformerBlock] After attention and residual connection: torch.Size([16, 7, 40])
[FeedForward] Input shape: torch.Size([16, 7, 40]), Performing feedforward transformations.
[FeedForward] Output shape: torch.Size([16, 7, 40])
[TransformerBlock] After feedforward and residual connection: torch.Size([16, 7, 40])
[TransformerEncoder] Processing layer 2
[TransformerBlock] Starting block processing. Input dimensions - value: torch.Size([16, 7, 40]), key: torch.Size([16, 7, 40]), query: torch.Size([16, 7, 40])
[MultiHeadAttention:1] Input shapes (V, K, Q) - values: torch.Size([16, 7, 40]), keys: torch.Size([16, 7, 40]), queries: torch.Size([16, 7, 40])
[MultiHeadAttention:2] After linear projections V/K/Q multihead- values: torch.Size([16, 7, 4, 10]), keys: torch.Size([16, 7, 4, 10]), queries: torch.Size([16, 7, 4, 10])
[MultiHeadAttention:3] Energy = Q * K (raw attention scores) shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:4] Applying mask with shape: torch.Size([16, 1, 1, 7])
[MultiHeadAttention:5] Attention SoftMax weights shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:6] Attention * V = Output shape after weighted sum: torch.Size([16, 7, 40])
[TransformerBlock] After attention and residual connection: torch.Size([16, 7, 40])
[FeedForward] Input shape: torch.Size([16, 7, 40]), Performing feedforward transformations.
[FeedForward] Output shape: torch.Size([16, 7, 40])
[TransformerBlock] After feedforward and residual connection: torch.Size([16, 7, 40])
[TransformerEncoder] Output x.shape: torch.Size([16, 7, 40])
[TransformerDecoder] Input x.shape: torch.Size([16, 7]), encoder_out.shape: torch.Size([16, 7, 40])
[PositionalEncoding] Input x.shape: torch.Size([16, 7, 40]), Adding positional encodings for sequence length and embedding size.
[PositionalEncoding] Output shape: torch.Size([16, 7, 40])

[TransformerDecoder] Processing layer 1
[TransformerDecoderBlock] x.shape: torch.Size([16, 7, 40]), encoder_out.shape: torch.Size([16, 7, 40])
[MultiHeadAttention:1] Input shapes (V, K, Q) - values: torch.Size([16, 7, 40]), keys: torch.Size([16, 7, 40]), queries: torch.Size([16, 7, 40])
[MultiHeadAttention:2] After linear projections V/K/Q multihead- values: torch.Size([16, 7, 4, 10]), keys: torch.Size([16, 7, 4, 10]), queries: torch.Size([16, 7, 4, 10])
[MultiHeadAttention:3] Energy = Q * K (raw attention scores) shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:4] Applying mask with shape: torch.Size([16, 1, 7, 7])
[MultiHeadAttention:5] Attention SoftMax weights shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:6] Attention * V = Output shape after weighted sum: torch.Size([16, 7, 40])
[MultiHeadAttention:1] Input shapes (V, K, Q) - values: torch.Size([16, 7, 40]), keys: torch.Size([16, 7, 40]), queries: torch.Size([16, 7, 40])
[MultiHeadAttention:2] After linear projections V/K/Q multihead- values: torch.Size([16, 7, 4, 10]), keys: torch.Size([16, 7, 4, 10]), queries: torch.Size([16, 7, 4, 10])
[MultiHeadAttention:3] Energy = Q * K (raw attention scores) shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:4] Applying mask with shape: torch.Size([16, 1, 1, 7])
[MultiHeadAttention:5] Attention SoftMax weights shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:6] Attention * V = Output shape after weighted sum: torch.Size([16, 7, 40])
[FeedForward] Input shape: torch.Size([16, 7, 40]), Performing feedforward transformations.
[FeedForward] Output shape: torch.Size([16, 7, 40])
[TransformerDecoderBlock] out.shape: torch.Size([16, 7, 40])

[TransformerDecoder] Processing layer 2
[TransformerDecoderBlock] x.shape: torch.Size([16, 7, 40]), encoder_out.shape: torch.Size([16, 7, 40])
[MultiHeadAttention:1] Input shapes (V, K, Q) - values: torch.Size([16, 7, 40]), keys: torch.Size([16, 7, 40]), queries: torch.Size([16, 7, 40])
[MultiHeadAttention:2] After linear projections V/K/Q multihead- values: torch.Size([16, 7, 4, 10]), keys: torch.Size([16, 7, 4, 10]), queries: torch.Size([16, 7, 4, 10])
[MultiHeadAttention:3] Energy = Q * K (raw attention scores) shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:4] Applying mask with shape: torch.Size([16, 1, 7, 7])
[MultiHeadAttention:5] Attention SoftMax weights shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:6] Attention * V = Output shape after weighted sum: torch.Size([16, 7, 40])
[MultiHeadAttention:1] Input shapes (V, K, Q) - values: torch.Size([16, 7, 40]), keys: torch.Size([16, 7, 40]), queries: torch.Size([16, 7, 40])
[MultiHeadAttention:2] After linear projections V/K/Q multihead- values: torch.Size([16, 7, 4, 10]), keys: torch.Size([16, 7, 4, 10]), queries: torch.Size([16, 7, 4, 10])
[MultiHeadAttention:3] Energy = Q * K (raw attention scores) shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:4] Applying mask with shape: torch.Size([16, 1, 1, 7])
[MultiHeadAttention:5] Attention SoftMax weights shape: torch.Size([16, 4, 7, 7])
[MultiHeadAttention:6] Attention * V = Output shape after weighted sum: torch.Size([16, 7, 40])
[FeedForward] Input shape: torch.Size([16, 7, 40]), Performing feedforward transformations.
[FeedForward] Output shape: torch.Size([16, 7, 40])
[TransformerDecoderBlock] out.shape: torch.Size([16, 7, 40])
[TransformerDecoder] Output x.shape: torch.Size([16, 7, 128])
[Main] Final output shape: torch.Size([16, 7, 128])
(.venv) sparkt@US-SPARKT-M3 attention_is_all_i_need % 
