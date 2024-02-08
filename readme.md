# Auto Captions for SDXL


This script can help you generate captions for a person or subject by using GPT-Vision. 


## Usage

First you must make sure you have your Open AI API key set. The program assumes it is set to `OPENAI_API_KEY`

You can temporary set it by running this:

```
export OPENAI_API_KEY=<YOUR_KEY>
```

You can expect to pay around $0.01 per image captioned. This is not a guarantee and you should check the Open AI pricing page.

After that is set up, clone the repo and run the caption command.

1. `git clone <REPO>`
2. `cd GPT-CAPTION-SDXL`
3. `python3 caption.py <token> <image_path>`

Replace token with what you want to use for the subject you are training. If you are not sure what to use, Google is your friend. There is a lot of discussions on the best tokens to use and that is far beyond the scope of this project.

Replace image_path with the path to the image folder you want to caption.

Then you can run the command like this:

```
python3 caption.py <token> <image_path>
```

### Example
```
python3 caption.py "sks" "C:\Users\user\training_data"
```
To change the extension of the output files, you can pass the `--ext` flag to the command.

```
python3 caption.py "sks" "C:\Users\user\training_data" --ext=md
```


### Optional parameters

| Parameter | Description | Default |
| --- | --- | --- |
| `--ext` | The extension of the output files | `txt` |



## Output

The outputted captions will be written to a `.txt` file that has the same name as the image it is captioning.

Example:

```
C:\Users\user\training_data\image1.jpg
C:\Users\user\training_data\image1.txt
```

This is perfect for using with [kohya_ss](https://github.com/bmaltais/kohya_ss)

If you would like to use a different caption you can pass the `--ext=<extension>` flag to the command. This will change the extension of the output files

## Notes

This script is not perfect and will not always generate the best captions. **Looking over the captions and making sure they are correct is important.**


## Roadmap

- [ ] Add more options for the captions
- [ ] Add style support

## License

I don't mind you taking this code and using it for your own projects. Its optional to give me credit, but it would be nice.

MIT License