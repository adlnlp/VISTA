# VISTA: Visual Storytelling enhanced Aspects

### <div align="center"> Hansel Matthew, Soyeon Caren Han, and Josiah Poon.</div>

## Aspect Enhanced Visual Storytelling Dataset
We introduce **VISTA**, a **visual storytelling** dataset with new **nine storytelling aspects** capturing creativity, emotion, and narrative richness, and propose a new metric, **VISTAScore**. This framework evaluates aspect expressiveness through combined lexical and semantic scorers. Using LVLMs and human validation, VISTA yields over **59k high-quality stories**.


## Dataset Details
VISTA dataset contained 59,407 stories, split into training, validation, and test sets with a 60/20/20 split: 35,644 for training, 11,881 for validation, and 11,882 for testing. Each data split is exported as a single JSON file, where each story is formatted as a JSON object using the following structure.

```json

{
    "Story ID": {
        "aspect": "Enhanced Story Aspect",
        "story": "dataset story",
        "image source": ["Image filenames sourced from VIST"]
    },
},

```

## Storytelling Aspects
Nine storytelling aspects chosen from our development process to represent diverse yet meaningful variations in human storytelling preferences.

| **Category** | **Aspect**    | **Description**                               | **Count** |
|--------------|---------------|-----------------------------------------------|-----------|
| **Style**    | Immersion     | Immerse reader deep into the story.           | 6909      |
|              | Clarity       | Convey the story clearly.                     | 6816      |
|              | Structure     | Use coherent narrative pathway.               | 6546      |
| **Storyline**| Setting       | Describe scenes effectively.                  | 6861      |
|              | Consistency   | Align the story traits and motivations.       | 6533      |
|              | Comedy        | Use of humour and twists.                     | 6927      |
| **Component**| Character     | Develop subjects’ roles/actions.              | 6307      |
|              | Objects       | Focus on key objects or events.               | 6917      |
|              | Relatability  | Express emotional relations of characters.    | 6909      |

## VISTAScore
We also introduce VISTAScore, a framework for evaluating the expressiveness of storytelling aspects in machine-generated stories. VISTAScore evaluates a candidate story against multiple references using three scorers: 
1. **N-gram Matching**  
   Measures lexical overlap to capture common word patterns linked to each aspect.
2. **Sentence-level Semantics**  
   Assesses similarity at the sentence level, accommodating different keywords or phrasing.
3. **Keyword-level Semantics**  
   Measures alignment with dominant aspect-specific keywords that strongly influence the narrative.

Our baseline experiment shows that models trained with VISTA outperform those trained on VIST across all aspects, achieving higher overall VISTAScores. This indicates that VISTA enables richer, more coherent, and more expressive narratives.
| Dataset              | Overall | Character | Clarity | Comedy | Consistency | Immersion | Objects | Relatability | Setting | Structure |
|----------------------|---------|-----------|---------|--------|-------------|-----------|---------|--------------|---------|-----------|
| **VIST**             | **0.5827** | 0.5746    | 0.5989  | 0.5679 | 0.5900      | 0.5706    | 0.5981  | 0.5907       | 0.5677  | 0.5854    |
| **VISTA (Our Data)** | **0.7894** | 0.7877    | 0.7933  | 0.7552 | 0.7956      | 0.7971    | 0.7959  | 0.8014       | 0.7955  | 0.7826    |

## Contributors
The contributors of the work are: 
- [Hansel Matthew](https://hnslmpweb.web.app) (Master of Data Science graduate at The University of Sydney)
- [Soyeon Caren Han](https://drcarenhan.github.io/) (Senior lecturer at The University of Melbourne)
- [Josiah Poon](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/josiah-poon) (Senior lecturer at The University of Sydney)