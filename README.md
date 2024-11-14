# Logit lens plot colab

[Try out your own prompts here.](https://colab.research.google.com/drive/1l6qN-hmCV4TbTcRZB5o6rUk_QPHBZb7K?usp=sharing)

# Installation

Set up a python environment and run
`pip install -r requirements.txt`

# Usage 

## Translation 

`papermill Translation.ipynb out.ipynb -p input_lang fr -p target_lang zh`

## Cloze

`papermill Cloze.ipynb out.ipynb -p target_lang fr`
## ******** NEW ADD(Reyhaneh's research)******:
Usage: you can run the cloze.ipynb with the ResearchInternshipRunningClozeTask.ipynb code. For different reasoning dataset, change the path of data in cloze.ipynb : df_en_de = pd.read_csv(f'{prefix}/yourpromptsfile.csv')

This project was used for analysing mathematical french prompts. Other datasets may need modification of cloze.ipynb code.

Results: You can see the results in results image file.


Conclusion:
The LLaMa 2 model processes and understands reasoning French data (English output after the layer 25) more slowly than regular non-reasoning French data (English output before the layer 25), resulting in delayed English output. This is not evident if we only consider the French output (blue chart), as there is no noticeable difference between the two diagrams when focusing solely on the blue chart.

# Precomputed latents

For your convenience, we also provide some precomputed latents on [huggingface.](https://huggingface.co/datasets/wendlerc/llm-latent-language) Here are some [preliminary steering experiments](https://colab.research.google.com/drive/1EhCk3_CZ_nSfxxpaDrjTvM-0oHfN9m2n?usp=sharing) using the precomputed latents.

# Acknowledgements

Starting point of this repo was [Nina Rimsky's](https://github.com/nrimsky/LM-exp/blob/main/intermediate_decoding/intermediate_decoding.ipynb) Llama-2 wrapper.

# Citation
```
@article{wendler2024llamas,
  title={Do Llamas Work in English? On the Latent Language of Multilingual Transformers},
  author={Wendler, Chris and Veselovsky, Veniamin and Monea, Giovanni and West, Robert},
  journal={arXiv preprint arXiv:2402.10588},
  year={2024}
}
```
