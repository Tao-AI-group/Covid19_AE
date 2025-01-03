# Annotated Dataset: Adverse Events following COVID-19 Vaccines from Social Media and VAERS

This dataset comprises annotated data on adverse events (AEs) following COVID-19 vaccination, sourced from VAERS, Twitter, and Reddit. It includes:

- **230 reports** from VAERS
- **3,383 tweets**
- **49 Reddit posts**

The dataset focuses on personal experiences of both short-term and long-term AEs, with named entity annotations for:

- **"vaccine"**: n = 4,244 
- **"shot"**: n = 2,715 
- **"ae" (adverse events)**: n = 7,567 

This data supports research in vaccine safety, public health monitoring, and biomedical natural language processing.

## File Structure

Each post/report in the dataset is accompanied by:

- A `.txt` file containing the original text
- A `.ann` file containing the annotation details

Both files share the same filename for the same post/report. All annotations were conducted using the [CLAMP annotation tool](https://clamp.uth.edu/).

## Reference Example

![Example Annotation](/clamp_annotation.png)

### Example

#### Original Post (in `.txt` file):
```text
My first shot of moderna vaccine = very sore arm the next day and very tired so I slept a lot.
```

#### Corresponding Annotation (in `.ann` file):
```text
T1	dose 3 13	first shot
T2	vaccine 17 32	moderna vaccine
T3	ae 40 48	sore arm
T4	ae 71 76	tired
T5	ae 82 93	slept a lot
```

### Explanation of Annotations:

1. **T1 (dose)**: "first shot" starts at character 3 and ends at character 13.
2. **T2 (vaccine)**: "moderna vaccine" starts at character 17 and ends at character 32.
3. **T3 (ae)**: "sore arm" starts at character 40 and ends at character 48.
4. **T4 (ae)**: "tired" starts at character 71 and ends at character 76.
5. **T5 (ae)**: "slept a lot" starts at character 82 and ends at character 93.

## Annotation Format

The `.ann` files use a standard format for NLP tasks:

- **Annotation ID**: Starts with "T" followed by a unique number (e.g., T1, T2).
- **Entity Type**: Categorizes the annotated text (e.g., dose, vaccine, ae).
- **Start and End Offsets**: Represent the character positions in the original text.
- **Text Span**: Contains the annotated text corresponding to the offsets.


## Citation

Please refer to the following paper for more details:

> Li, Yiming, Deepthi Viswaroopan, William He, Jianfu Li, Xu Zuo, Hua Xu, and Cui Tao. "Improving Entity Recognition using ensembles of Deep Learning and Fine-tuned large Language models: a case study on adverse event extraction from multiple sources." *arXiv preprint arXiv:2406.18049* (2024). [https://doi.org/10.48550/arXiv.2406.18049](https://doi.org/10.48550/arXiv.2406.18049)

For reuse of this dataset, please cite the following works:

1. Li, Yiming, Deepthi Viswaroopan, William He, Jianfu Li, Xu Zuo, Hua Xu, and Cui Tao. "Improving Entity Recognition using ensembles of Deep Learning and Fine-tuned large Language models: a case study on adverse event extraction from multiple sources." *arXiv preprint arXiv:2406.18049* (2024). [https://doi.org/10.48550/arXiv.2406.18049](https://doi.org/10.48550/arXiv.2406.18049)

2. Lian, Andrew T., Jingcheng Du, and Lu Tang. 2022. "Using a Machine Learning Approach to Monitor COVID-19 Vaccine Adverse Events (VAE) from Twitter Data." *Vaccines 10 (1): 103.* [https://doi.org/10.3390/vaccines10010103](https://doi.org/10.3390/vaccines10010103)
