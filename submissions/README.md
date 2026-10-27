# Submissions

One row per submission to the leaderboard, as described in the [README](../README.md#submitting-a-model-to-the-leaderboard).

| Model | Board | Model repo | Results | Engine and settings | Hardware |
|---|---|---|---|---|---|
| Xing-VL2.0-Decision (renamed from RBDash-Decision-v0.2, #262; rename request #279) | **vision** | [RBDash-Team/Xing-VL2.0-Decision](https://huggingface.co/RBDash-Team/Xing-VL2.0-Decision) @ cdc66b0 | [runs/vision-rbdash-decision-v0.2/vision-scores.json](https://huggingface.co/datasets/RBDash-Team/decision-index-results/blob/main/runs/vision-rbdash-decision-v0.2/vision-scores.json) (complete, public vision index 77.78, unchanged) | Unchanged from #262: custom engine `rbdash_decision_engine:RBDashEngine` shipped in the model repo, driven through `decision-index vision pipeline` at commit `f5a6e4f`. Native classification: one forward pass, 255-way readout over the option codes, temperature 0.9766 from `decision_config.json`. bfloat16, native resolution capped at 1,638,400 pixels per image, one to four images, nothing truncated. | 1x A800-SXM4-80GB |

This is a rename only. The model repo was renamed in place on the Hub (the old id `RBDash-Team/RBDash-Decision-v0.2` redirects to it), the weights are byte-identical, and nothing was retrained, re-run or re-scored.
