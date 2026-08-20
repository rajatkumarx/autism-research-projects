# SPARK Autism-Related Research Dataset

A collection of autism-related research projects developed under the Social and Personal Adaptive Response Kit (SPARK) initiative at King Abdullah University of Science and Technology (KAUST). The projects investigate artificial intelligence, wearable sensing, and human body communication technologies to support children with autism spectrum disorder (ASD).


## Dataset Overview

This repository contains ZIP archives of CSV files with five-second time-series recordings of inertial measurement unit (IMU) pitch and roll signals collected from wrist-worn sensors during controlled activities. The data were not collected from autistic individuals. Instead, they were collected from individuals who mimicked or simulated selected autism-related behaviors for research and algorithm-development purposes. Therefore, this dataset should not be considered clinically representative of individuals with autism spectrum disorder (ASD), and results should not be generalized to autistic individuals without appropriate validation. Users are responsible for complying with all applicable ethical, privacy, data-protection, and institutional review/ethics board requirements when accessing and analyzing this dataset.


## Directory Naming Convention

Directory names use abbreviations describing the subject group, sensor location, and activity.
- Subject group: `S01` (Subject 01), `Sxx` (multiple subjects).
- Sensor location: `RW` (right wrist), `LW` (left wrist).
- Activity: one of the activity labels below (e.g., `arm`, `hair`, `hand`, `mouth`, `random`).


## Activity Labels

The current activity categories are:
- Arm flapping (`arm`).
- Hair twisting or pulling (`hair`).
- Hand flapping (`hand`).
- Mouthing (`mouth`).
- Random activities (`random`).

The `random` category represents activities other than the specific behaviors listed above. Researchers should describe the composition of this category when reporting results, since its variability may differ from that of the more targeted activity classes.


## Sampling Rates

Sampling rates differ by sensor location.
- Left wrist (`LW`): approximately 4 Hz
- Right wrist (`RW`): approximately 26 Hz.

Each recording lasts approximately 5 s. Consequently, the number of samples may differ between sensor locations. Verify the sampling rate and sample count from the CSV files before analysis.


## CSV File Format

Typical columns in the CSV files in this dataset are:

| Column  | Description                           | Unit    |
|-------- |---------------------------------------|---------|
| `time`  | Time from the start of the recording  | s       |
| `pitch` | Pitch angle                           | degrees |
| `roll`  | Roll angle                            | degrees |


## Recommended Use

Before analysis, researchers should:
- Validate the CSV format, recording duration, and sample count.
- Account for the different left- and right-wrist sampling rates.
- Document filtering, normalization, resampling, and missing-value handling.


## Citation

Users of this dataset are requested to cite the associated SPARK project publication.

```bibtex
@ARTICLE{kumar2026stereotypic,
  author={Kumar, Rajat and Ali, Abdelhay and Eltawil, Ahmed M.},
  journal={IEEE Sensors Journal}, 
  title={Stereotypic Repetitive Behavior Monitoring Using Human Body Communication}, 
  year={2026},
  volume={26},
  number={16},
  pages={24802-24817},
  doi={10.1109/JSEN.2026.3705190}}
```

## License

The intended use and restrictions are:
- The data may be used for methodological, algorithm-development, and research purposes.
- The data must not be used for clinical diagnosis, clinical decision-making, or claims of clinical efficacy.
- The data must not be used to attempt to identify or re-identify any individual participant.
- Any publications or derivative datasets must cite the associated publication as described above.
- Commercial use (including use in commercial products or services) is prohibited.
