# Proposal revision to-do (after sidang proposal, 25 Sep 2026)

Result: passed, with revisions. Page numbers below are the printed page numbers of the proposal PDF.

## 0. Decide first (changes the numbers everywhere)
- [ ] Decide: add more images and re-split now, or update with the current numbers and mark "to be extended"
- [ ] If you re-split: keep duplicates/near-duplicates/same-source images in the same split, then re-run the dataset summary script
- [ ] Current numbers: 133 images (107/13/13), 613 instances (495/61/57), 9 classes

## 1. Proposal document
- [x] 3.1.1.1 (p.28): replace ">300 images kept" with the funnel: 21 reference, 392 crawled candidates, >300 after first cleaning, 133 final after second manual selection
- [x] 3.1.1.1: state the real reason images were removed (fill in yourself)
- [x] 3.1.1.3 (p.31): change 70/15/15 to the real split, 107/13/13 images (about 80/10/10), 495/61/57 instances
- [x] 3.1.1.4 (p.31-32): add rotation to the augmentation list (examiner asked for it)
- [x] 3.1.1.4: reword "perubahan warna" to brightness/saturation variation with only a small hue shift
- [x] 3.1.1.4: add a figure of augmented samples (Ultralytics usually saves train_batch*.jpg in the run folder)
- [x] 3.1.2 (p.33): add USB webcam, touchscreen, embedded system target, laptop (Ryzen 7 4800H, RTX 3050, 16GB DDR4), Google Colab, Qt/QML; say the embedded environment is simulated on the laptop because of hardware cost
- [x] Add assumption sentence: "Sistem dirancang dengan asumsi pelanggan tidak sengaja menyembunyikan atau menumpuk lauk untuk menghindari penghitungan; tumpang tindih alami antar lauk tetap menjadi keterbatasan yang dievaluasi."
- [x] Figure 2.1 (p.10): the price database is drawn inside the flow; show it as a side lookup only (examiner was confused)
- [x] 3.1.3.2 (p.35-36): add one sentence that the price table is only looked up, not part of image processing
- [x] Use the same prices in Table 3.1 (rendang Rp20.000) and Figure 3.6 (rendang Rp10.000)
- [x] Add one short justification for YOLO11-seg over v12 (better documented and tested for segmentation)


## 2. Work, not document
- [ ] Measure inference time per image (on the laptop; on the embedded target if you get one)
- [ ] Collect about 100 more images, mainly telur dadar, ayam goreng, daun singkong

## 3. Ask your advisor
- [ ] Per-class table and class imbalance: include or not, and how to word it
- [ ] Start with 4-5 classes first, or keep 9?
- [ ] How many images are enough?
- [ ] Is cross-validation acceptable given the small test set?
- [ ] Pricing assumptions (for example sambal free, nasi included)
