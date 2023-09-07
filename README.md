# QASiNa: Question Answering Sirah Nabawiyah Dataset

## Dataset Summary

Question Answering Sirah Nabawiyah Dataset (QASiNa) is Extractive QA Dataset which build to perform QA task in Sirah Nabawiyah domain.

## Languages

Language: Indonesian

## Dataset Format

There are two dataset format, in JSON and CSV format with the same data

### CSV columns

- **ID** : Question ID (integer)
- **cotext_id** : Context ID (integer)
- **context_title** : Context title (string)
- **context_length** : Length of context (integer)
- **context** : Full text of context (string)
- **question** : Question sentence (string)
- **answer** : Answer sentence (string)
- **start position** : Starting position of answer sentence (integer)
- **question type** : Type of question (string)

### JSON format

```
{
    "context_id": unique integer,
    "context": string,
    "question_answers": [
      {
        "type": what / who / where / how many / when,
        "question": string,
        "answer": string,
        "answer_start": integer,
        "question_id": unique integer
      },
    "context_length": integer,
    "context_title": string
  }
```

## Data Example


### JSON example
```py
{
    "context_id": 0,
    "context": "Pada saat Nabi sudah hijrah ke Madinah masih sering terjadi peperangan antara orang Islam dengan kafir Quraisy, diantaranya adalah perang Badar. Perang badar merupakan salah satu perang yang sangat menentukan masa depan negara Islam yang terjadi pada tahun kedua di daerah Badar kurang lebih 120 km dari Madinah. Perang badar ada tiga macam, yaitu perang badar pertama, perang badar kubra, dan perang badar yang terakhir (Ghazwah al-Sawiq) terjadi pada abad keempat hijrah. Perang badar kubra didahului oleh Sariyah Abdullah Ibn Jahsy ke daerah Nakhlah yang berada di antara Mekkah dan Thaif yang terjadi pada bulan Rajab tahun ke-2 H. Sariyah inilah yang menjadi penyebab paling kuat terhadap perang Badar Kubra.",
    "question_answers": [
      {
        "type": "who",
        "question": "Siapa yang menjadi penyebab terjadinya perang Badar Kubra?",
        "answer": "Sariyah Abdullah Ibn Jahsy",
        "answer_start": 508,
        "question_id": 0
      },
      {
        "type": "when",
        "question": "Kapan perang Badar terjadi?",
        "answer": "tahun kedua",
        "answer_start": 251,
        "question_id": 1
      },
      {
        "type": "what",
        "question": "Apa saja macam-macam perang Badar yang terjadi?",
        "answer": "perang badar pertama, perang badar kubra, dan perang badar yang terakhir (Ghazwah al-Sawiq)",
        "answer_start": 348,
        "question_id": 2
      }
    ],
    "context_length": 713,
    "context_title": "Penyebab Perang Badar (1)"
  }
```
