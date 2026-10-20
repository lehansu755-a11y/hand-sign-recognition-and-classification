# Hand Sign Recognition and Classification

Supervisor: Dr Adam Schiffer

## My interpretation of the brief

I understand this project as developing a camera-based system that detects a hand and classifies its pose into a predefined set of hand signs.

My initial idea is to collect labelled examples of different hand poses within a defined camera working range, store the samples or their extracted features, and use them to recognise signs in a live camera stream. Each sign would have multiple examples rather than a single reference image.

The system would detect the hand, extract useful features, and classify the pose using feature matching or a trained classifier. Hand size and camera distance should be addressed through scale normalisation, so recognition depends mainly on relative finger positions and hand shape.

I would initially focus on static signs. Recognising a sign and evaluating how closely it follows a reference pose are separate tasks; pose-quality scoring would be a possible later extension.

## Why I am a good fit for this project

I am interested in how a computer can learn from recorded examples and recognise a new hand pose in real time.

In particular, I would like to investigate whether the same sign can be recognised reliably when performed by different people, at different distances, or with small variations in finger position.

I am also interested in allowing users to record a small set of custom signs and later recognise those signs through a webcam. This provides a practical motivation for investigating sample collection, feature representation, and classification.

## Relevant experience and background

Through this project, I would like to develop my knowledge of computer vision, feature extraction, supervised classification, and real-time image processing.

I would begin with a manageable prototype and improve it through systematic experiments. The final tools and implementation scope would be agreed with the supervisor.

## Proposed approach

I would first confirm the topic requirements with the supervisor and select a limited set of distinguishable static signs.

The proposed pipeline is webcam capture, hand detection, feature extraction and normalisation, classification, and live result display. Possible features include relative landmark positions, finger angles, and distance ratios.

For each sign, I would collect multiple labelled examples with variations in pose and recording conditions. A simple feature-matching baseline would be compared with a suitable supervised classifier. The dataset, preprocessing settings, and model would be saved for reproducibility.

The interface would display the recognised sign and handle no-hand and uncertain-pose cases. Classification confidence would not automatically be interpreted as a measure of pose correctness.

Evaluation would include accuracy, per-class precision and recall, a confusion matrix, and processing latency. Separate recording sessions and, where feasible, held-out participants would be used for testing, avoiding random splits of near-identical video frames.

## Initial plan

1. Confirm the requirements, sign vocabulary, and evaluation objectives with the supervisor.
2. Review suitable hand-detection and classification methods.
3. Build a webcam capture and hand-feature extraction prototype.
4. Collect and label an initial dataset.
5. Implement normalisation and a recognition baseline.
6. Train and compare a suitable classifier using separate training, validation, and test data.
7. Integrate live recognition and uncertain-pose handling.
8. Evaluate different people, camera distances, and lighting conditions.
9. Document the results, limitations, and possible improvements.

## Additional information

The proposed initial scope is single-hand static sign classification using an ordinary webcam and a limited sign vocabulary. Dynamic gestures and full sign-language translation would require additional scope.

My main interest is preserving meaningful differences between signs while reducing the effects of hand size, camera distance, and small variations in execution.

Possible extensions include custom user-defined signs, additional classifiers, and a separately defined pose-similarity score.

Project repository: https://github.com/lehansu755-a11y/hand-sign-recognition-and-classification

This is an application draft. The official topic identifier and exact uploaded template still require verification.
