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

## Contributors
The contributors of the work are: 
- [Hansel Matthew](https://hnslmpweb.web.app) (Master of Data Science graduate at The University of Sydney)
- [Soyeon Caren Han](https://drcarenhan.github.io/) (Senior lecturer at The University of Melbourne)
- [Josiah Poon](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/josiah-poon) (Senior lecturer at The University of Sydney)