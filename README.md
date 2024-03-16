{
  "type": "object",
  "title": "Input",
  "properties": {
    "seed": {
      "type": "integer",
      "title": "Seed",
      "x-order": 8,
      "description": "Fix the random seed for reproducibility"
    },
    "image": {
      "type": "string",
      "title": "Image",
      "format": "uri",
      "x-order": 0,
      "description": "An image of a person to be converted"
    },
    "style": {
      "enum": [
        "3D",
        "Emoji",
        "Video game",
        "Pixels",
        "Clay",
        "Toy"
      ],
      "type": "string",
      "title": "style",
      "description": "Style to convert to",
      "default": "3D",
      "x-order": 1
    },
    "prompt": {
      "type": "string",
      "title": "Prompt",
      "default": "a person",
      "x-order": 2
    },
    "lora_scale": {
      "type": "number",
      "title": "Lora Scale",
      "default": 1,
      "maximum": 1,
      "minimum": 0,
      "x-order": 10,
      "description": "How strong the LoRA will be"
    },
    "custom_lora_url": {
      "type": "string",
      "title": "Custom Lora Url",
      "x-order": 9,
      "description": "URL to a Replicate custom LoRA. Must be in the format https://replicate.delivery/pbxt/[id]/trained_model.tar or https://pbxt.replicate.delivery/[id]/trained_model.tar"
    },
    "negative_prompt": {
      "type": "string",
      "title": "Negative Prompt",
      "default": "",
      "x-order": 3,
      "description": "Things you do not want in the image"
    },
    "prompt_strength": {
      "type": "number",
      "title": "Prompt Strength",
      "default": 4.5,
      "maximum": 20,
      "minimum": 0,
      "x-order": 5,
      "description": "Strength of the prompt. This is the CFG scale, higher numbers lead to stronger prompt, lower numbers will keep more of a likeness to the original."
    },
    "denoising_strength": {
      "type": "number",
      "title": "Denoising Strength",
      "default": 0.65,
      "maximum": 1,
      "minimum": 0,
      "x-order": 4,
      "description": "How much of the original image to keep. 1 is the complete destruction of the original image, 0 is the original image"
    },
    "instant_id_strength": {
      "type": "number",
      "title": "Instant Id Strength",
      "default": 1,
      "maximum": 1,
      "minimum": 0,
      "x-order": 7,
      "description": "How strong the InstantID will be."
    },
    "control_depth_strength": {
      "type": "number",
      "title": "Control Depth Strength",
      "default": 0.8,
      "maximum": 1,
      "minimum": 0,
      "x-order": 6,
      "description": "Strength of depth controlnet. The bigger this is, the more controlnet affects the output."
    }
  }
}
