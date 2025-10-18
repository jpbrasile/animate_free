# animate_free
création audio, image, video avec les meilleurs outils 

## <a href="https://github.com/dvlab-research/DreamOmni2">DreamOmni2</a>

<img src="https://github.com/dvlab-research/DreamOmni2/blob/main/imgs/gallery.png?raw=true" alt="your-alt-text" width="500"/>

Pour l'installer 
- Suivez les instructions
- Quand il y a un problème:
  - Couper coller le problème dans <a href="https://aistudio.google.com/">AI Studio</a>
  - Suivez les instructions , par exemple :
 
  Excellent question. Yes, you absolutely need initial images to run the `inference_edit.py` script.

The script is designed for **image editing and composition**, so it needs input images to work on. Based on the command you were trying to run, it specifically requires **two** images:

1.  **A Source Image (`src.jpg`):** This is the main background or scene you want to modify. In your example command, this is the image of the road.
2.  **A Reference Image (`ref.jpg`):** This image contains the object, person, or style that you want to transfer *into* the source image. In your example, this is the image of the woman.

### Where to Find the Example Images

The paths in the command tell you exactly where the script expects to find them. Since your current directory is `DreamOmni2`, the paths are relative to that location.

Here is the expected folder structure inside your `DreamOmni2` workspace:

```
DreamOmni2/
├── example_input/
│   └── edit_tests/
│       ├── src.jpg      <-- The source image (the road)
│       └── ref.jpg      <-- The reference image (the woman)
├── inference_edit.py    <-- The script you are running
└── ... (other files and folders like README.md, etc.)
```

**Action for you:**
Please check if you have the `example_input` folder and the images inside it. These should have come with the project when you downloaded or cloned it from GitHub. If they are missing, you may need to re-download the project or check if there's a separate download link for the example data.

### How to Use Your Own Images

When you are ready to use your own pictures, you can follow these steps:

1.  **Place Your Images:** Create a new folder inside `DreamOmni2`, for example, named `my_images`. Put your source and reference images in there. Let's say you have `my_background.png` and `my_character.jpg`.

2.  **Modify the Command:** You would then change the paths in the command to point to your new files. You would also update the instruction to describe what you want to do.

**Example with your own images:**

```powershell
python inference_edit.py `
  --input_img_path "my_images/my_background.png" "my_images/my_character.jpg" `
  --input_instruction "Put the character from the second image into the background of the first image." `
  --output_path "my_images/result.png"
```

For now, assuming the example files (`src.jpg` and `ref.jpg`) exist in the correct location, you are ready to run the corrected command from our previous conversation.

- En fait l'image du chemin est là :DreamOmni2\example_input\edit_tests\src.jpg
et l'image de la femme ici : DreamOmni2\example_input\edit_tests\ref.jpg
- Donne le script pour le mix

  Parfait ! Les images sont exactement là où le script s'attend à les trouver. Vous êtes prêt à lancer la commande.

Voici le script complet pour "mixer" les deux images.

Assurez-vous que votre terminal est bien dans le dossier `DreamOmni2` (comme c'est le cas actuellement), puis copiez et collez la commande suivante **en une seule ligne** et appuyez sur Entrée.

### Le Script à Exécuter

```powershell
python inference_edit.py --input_img_path "example_input/edit_tests/src.jpg" "example_input/edit_tests/ref.jpg" --input_instruction "Make the woman from the second image stand on the road in the first image." --output_path "example_input/edit_tests/edit_res.png"
```

### Que va-t-il se passer ?

1.  Le script va démarrer. Cela peut prendre un peu de temps pour charger le modèle.
2.  Il va prendre l'image `src.jpg` (la route) comme fond.
3.  Il va prendre l'image `ref.jpg` (la femme) comme référence.
4.  Il suivra l'instruction en anglais : "Faites en sorte que la femme de la deuxième image se tienne sur la route de la première image."
5.  Une fois le traitement terminé, une nouvelle image nommée **`edit_res.png`** sera créée dans le dossier `DreamOmni2\example_input\edit_tests\`.

C'est tout ! Lancez cette commande et vous devriez obtenir votre image mixée.

## Upscaling video avec <a href="https://github.com/xh9998/DiffVSR">DiffVSR</a> 

<img src="https://github.com/xh9998/DiffVSR/blob/master/assets/teaser.png?raw=true" alt="your-alt-text" width="500"/>





