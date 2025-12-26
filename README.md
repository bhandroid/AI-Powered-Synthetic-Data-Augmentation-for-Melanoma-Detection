# AI-Powered-Synthetic-Data-Augmentation-for-Melanoma-Detection
Medical image classification suffers from severe class imbalance, particularly for rare but
critical conditions like melanoma. This project leverages StyleGAN2 to generate synthetic
melanoma images, addressing the 6:1 imbalance between benign nevi and melanoma in
the HAM10000 dataset. We trained StyleGAN2 on 779 melanoma samples, generated
1,000 synthetic images, and applied discriminator-based quality filtering to select the top
300 high-quality samples.
Three ResNet50 classifiers were trained: baseline (7,010 real images), filtered
augmentation (+300 synthetic), and unfiltered augmentation (+1,000 synthetic). The
filtered approach achieved the best results: 90.55% accuracy (+3.12% vs baseline) and
71.86% melanoma recall (+5.39% vs baseline), representing ~5 additional melanoma
detections per 100 patients. Critically, quality filtering proved essential—300 high-quality
images outperformed 1,000 mixed-quality images across all metrics.
This work demonstrates that synthetic medical data augmentation can provide clinically
meaningful improvements when coupled with rigorous quality control, offering a privacypreserving solution to data scarcity in medical AI.
