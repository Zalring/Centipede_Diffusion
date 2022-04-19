# Centipede Diffusion (Disco Diffusion 5.2 + Latent Diffusion LAION-400M model)

Connect the Latent Diffusion (LD) output to the Disco Diffusion (DD) input, in order to generate coherent and artistic images and animations.

In short, LL creates a cohesive overall shape. Then DD adds the details and brings the artistic touch to the final result.

Useful information about this notebook:
- As the sum of the Disco Diffusion 5.2 and Latent Diffusion LAION-400M notebooks, it needs a lot of GPU RAM to run properly (successfully tested with a T4 and a P100 for the defaults settings) and may require a Pro account. Also, you'll maybe need to pay (a little) for more space on your drive.
- As it sums the parameters of the both notebooks, there is two prompts to fill! Of course, you can use the same prompt two times, but it's possible to vary to get (or not) interesting results.
- A tip about that for human lookalike faces generation: use the name of a famous painter known for his portraits (best I found is Rembrandt) in the prompt_1 (LD), and put the modifiers words that focus on the details and the desired style in the prompt_2 (DD).
- A tick in a checkbox allows you to pause the generation between the LD part and the DD part in order to select which LD outputs you want to include as inputs in the batch of DD (with an index list parameter). I find it's more convenient to allow a human intervention at this point to filter the potentially "bad" results, as LD is fast at generating many images and easy to reroll where DD can be slow in comparison.
- The size of the DD generated image is expressed as a multiple of the LD generated ones.
- For the most impacting parameters of DD, it is possible to define a list, mapping to each element of the batch, in order to facilitate the tests.
- 3D Animations with Turbo mode work (they only use the first input image of the list), but I haven't try for the other animations modes and options.

Link to the notebook :

https://colab.research.google.com/github/Zalring/Centipede_Diffusion/blob/main/Centipede_Diffusion.ipynb

Links to the source notebooks :

https://colab.research.google.com/github/alembics/disco-diffusion/blob/main/Disco_Diffusion.ipynb

https://colab.research.google.com/github/multimodalart/latent-diffusion-notebook/blob/main/Latent_Diffusion_LAION_400M_model_text_to_image.ipynb
