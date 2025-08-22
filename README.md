[correctornot (1).json](https://github.com/user-attachments/files/21931512/correctornot.1.json)
{
  "id": "2e78b4fb-9006-4383-aad3-a762d17ff1dd",
  "revision": 0,
  "last_node_id": 112,
  "last_link_id": 210,
  "nodes": [
    {
      "id": 66,
      "type": "ModelSamplingAuraFlow",
      "pos": [
        550,
        20
      ],
      "size": [
        290,
        60
      ],
      "flags": {},
      "order": 11,
      "mode": 0,
      "inputs": [
        {
          "name": "model",
          "type": "MODEL",
          "link": 185
        }
      ],
      "outputs": [
        {
          "name": "MODEL",
          "type": "MODEL",
          "links": [
            141
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.48",
        "Node name for S&R": "ModelSamplingAuraFlow",
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "widget_ue_connectable": {}
      },
      "widgets_values": [
        3
      ]
    },
    {
      "id": 88,
      "type": "VAEEncode",
      "pos": [
        370,
        630
      ],
      "size": [
        140,
        46
      ],
      "flags": {},
      "order": 12,
      "mode": 0,
      "inputs": [
        {
          "name": "pixels",
          "type": "IMAGE",
          "link": 178
        },
        {
          "name": "vae",
          "type": "VAE",
          "link": 200
        }
      ],
      "outputs": [
        {
          "name": "LATENT",
          "type": "LATENT",
          "links": [
            206
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.50",
        "Node name for S&R": "VAEEncode",
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "ue_properties": {
          "widget_ue_connectable": {}
        }
      },
      "widgets_values": []
    },
    {
      "id": 97,
      "type": "MarkdownNote",
      "pos": [
        550,
        780
      ],
      "size": [
        300,
        190
      ],
      "flags": {},
      "order": 0,
      "mode": 0,
      "inputs": [],
      "outputs": [],
      "title": "KSampler settings",
      "properties": {},
      "widgets_values": [
        "You can test and find the best setting by yourself. The following table is for reference.\n\n| Model            | Steps | CFG |\n|---------------------|---------------|---------------|\n| Offical             | 50               | 4.0               \n| fp8_e4m3fn             | 20                | 2.5               |\n| fp8_e4m3fn + 4steps LoRA    | 4               | 1.0               |\n"
      ],
      "color": "#432",
      "bgcolor": "#653"
    },
    {
      "id": 96,
      "type": "MarkdownNote",
      "pos": [
        -210,
        1020
      ],
      "size": [
        280,
        88
      ],
      "flags": {},
      "order": 1,
      "mode": 0,
      "inputs": [],
      "outputs": [],
      "properties": {},
      "widgets_values": [
        "This node is to avoid poor output results caused by excessively large input image sizes."
      ],
      "color": "#432",
      "bgcolor": "#653"
    },
    {
      "id": 107,
      "type": "UnetLoaderGGUF",
      "pos": [
        -89.97850799560547,
        -103.78764343261719
      ],
      "size": [
        270,
        58
      ],
      "flags": {},
      "order": 2,
      "mode": 0,
      "inputs": [],
      "outputs": [
        {
          "name": "MODEL",
          "type": "MODEL",
          "links": [
            196
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfyui-gguf",
        "ver": "1.1.4",
        "Node name for S&R": "UnetLoaderGGUF"
      },
      "widgets_values": [
        "Qwen_Image_Edit-Q4_K_S.gguf"
      ]
    },
    {
      "id": 39,
      "type": "VAELoader",
      "pos": [
        -263.49383544921875,
        371.5661315917969
      ],
      "size": [
        330,
        60
      ],
      "flags": {},
      "order": 3,
      "mode": 0,
      "inputs": [],
      "outputs": [
        {
          "name": "VAE",
          "type": "VAE",
          "slot_index": 0,
          "links": [
            197,
            198,
            199,
            200
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.48",
        "Node name for S&R": "VAELoader",
        "models": [
          {
            "name": "qwen_image_vae.safetensors",
            "url": "https://huggingface.co/Comfy-Org/Qwen-Image_ComfyUI/resolve/main/split_files/vae/qwen_image_vae.safetensors",
            "directory": "vae"
          }
        ],
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "widget_ue_connectable": {}
      },
      "widgets_values": [
        "Qwen_Image-VAE.safetensors"
      ]
    },
    {
      "id": 104,
      "type": "PreviewImage",
      "pos": [
        1055.439208984375,
        292.8052673339844
      ],
      "size": [
        140,
        246
      ],
      "flags": {},
      "order": 18,
      "mode": 0,
      "inputs": [
        {
          "name": "images",
          "type": "IMAGE",
          "link": 189
        }
      ],
      "outputs": [],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.50",
        "Node name for S&R": "PreviewImage"
      },
      "widgets_values": []
    },
    {
      "id": 89,
      "type": "LoraLoaderModelOnly",
      "pos": [
        170,
        30
      ],
      "size": [
        270,
        82
      ],
      "flags": {},
      "order": 9,
      "mode": 0,
      "inputs": [
        {
          "name": "model",
          "type": "MODEL",
          "link": 196
        }
      ],
      "outputs": [
        {
          "name": "MODEL",
          "type": "MODEL",
          "links": [
            185
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.50",
        "Node name for S&R": "LoraLoaderModelOnly",
        "models": [
          {
            "name": "Qwen-Image-Lightning-4steps-V1.0.safetensors",
            "url": "https://huggingface.co/lightx2v/Qwen-Image-Lightning/resolve/main/Qwen-Image-Lightning-4steps-V1.0.safetensors",
            "directory": "loras"
          }
        ],
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "ue_properties": {
          "widget_ue_connectable": {
            "lora_name": true,
            "strength_model": true
          }
        }
      },
      "widgets_values": [
        "Qwen-Image-Lightning-8steps-V1.1.safetensors",
        1
      ]
    },
    {
      "id": 38,
      "type": "CLIPLoader",
      "pos": [
        -250,
        170
      ],
      "size": [
        330,
        110
      ],
      "flags": {},
      "order": 4,
      "mode": 0,
      "inputs": [],
      "outputs": [
        {
          "name": "CLIP",
          "type": "CLIP",
          "slot_index": 0,
          "links": [
            203,
            204
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.48",
        "Node name for S&R": "CLIPLoader",
        "models": [
          {
            "name": "qwen_2.5_vl_7b_fp8_scaled.safetensors",
            "url": "https://huggingface.co/Comfy-Org/Qwen-Image_ComfyUI/resolve/main/split_files/text_encoders/qwen_2.5_vl_7b_fp8_scaled.safetensors",
            "directory": "text_encoders"
          }
        ],
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "widget_ue_connectable": {}
      },
      "widgets_values": [
        "qwen_2.5_vl_7b_fp8_scaled.safetensors",
        "qwen_image",
        "default"
      ]
    },
    {
      "id": 109,
      "type": "ClipLoaderGGUF",
      "pos": [
        -547.52783203125,
        144.002197265625
      ],
      "size": [
        270,
        106
      ],
      "flags": {},
      "order": 5,
      "mode": 0,
      "inputs": [],
      "outputs": [
        {
          "name": "CLIP",
          "type": "CLIP",
          "links": []
        }
      ],
      "properties": {
        "cnr_id": "gguf",
        "ver": "2.4.0",
        "Node name for S&R": "ClipLoaderGGUF"
      },
      "widgets_values": [
        "Qwen2.5-VL-7B-Instruct-IQ4_XS.gguf",
        "qwen_image",
        "default"
      ]
    },
    {
      "id": 93,
      "type": "ImageScaleToTotalPixels",
      "pos": [
        -134.9154510498047,
        899.5345458984375
      ],
      "size": [
        270,
        82
      ],
      "flags": {},
      "order": 10,
      "mode": 0,
      "inputs": [
        {
          "name": "image",
          "type": "IMAGE",
          "link": 177
        }
      ],
      "outputs": [
        {
          "name": "IMAGE",
          "type": "IMAGE",
          "links": [
            178,
            179,
            180
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.50",
        "Node name for S&R": "ImageScaleToTotalPixels",
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "ue_properties": {
          "widget_ue_connectable": {
            "upscale_method": true,
            "megapixels": true
          }
        }
      },
      "widgets_values": [
        "lanczos",
        1
      ]
    },
    {
      "id": 8,
      "type": "VAEDecode",
      "pos": [
        890,
        20
      ],
      "size": [
        210,
        46
      ],
      "flags": {
        "collapsed": false
      },
      "order": 17,
      "mode": 0,
      "inputs": [
        {
          "name": "samples",
          "type": "LATENT",
          "link": 207
        },
        {
          "name": "vae",
          "type": "VAE",
          "link": 199
        }
      ],
      "outputs": [
        {
          "name": "IMAGE",
          "type": "IMAGE",
          "slot_index": 0,
          "links": [
            189
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.48",
        "Node name for S&R": "VAEDecode",
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "widget_ue_connectable": {}
      },
      "widgets_values": []
    },
    {
      "id": 75,
      "type": "CFGNorm",
      "pos": [
        550,
        130
      ],
      "size": [
        290,
        60
      ],
      "flags": {},
      "order": 15,
      "mode": 0,
      "inputs": [
        {
          "name": "model",
          "type": "MODEL",
          "link": 141
        }
      ],
      "outputs": [
        {
          "name": "patched_model",
          "type": "MODEL",
          "links": [
            208
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.50",
        "Node name for S&R": "CFGNorm",
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "ue_properties": {
          "widget_ue_connectable": {
            "strength": true
          }
        }
      },
      "widgets_values": [
        1
      ]
    },
    {
      "id": 76,
      "type": "TextEncodeQwenImageEdit",
      "pos": [
        140,
        200
      ],
      "size": [
        360,
        150
      ],
      "flags": {},
      "order": 13,
      "mode": 0,
      "inputs": [
        {
          "name": "clip",
          "type": "CLIP",
          "link": 203
        },
        {
          "name": "vae",
          "shape": 7,
          "type": "VAE",
          "link": 197
        },
        {
          "name": "image",
          "shape": 7,
          "type": "IMAGE",
          "link": 179
        }
      ],
      "outputs": [
        {
          "name": "CONDITIONING",
          "type": "CONDITIONING",
          "links": [
            209
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.50",
        "Node name for S&R": "TextEncodeQwenImageEdit",
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "ue_properties": {
          "widget_ue_connectable": {
            "prompt": true
          }
        }
      },
      "widgets_values": [
        "change the background to a beach"
      ],
      "color": "#232",
      "bgcolor": "#353"
    },
    {
      "id": 77,
      "type": "TextEncodeQwenImageEdit",
      "pos": [
        140,
        400
      ],
      "size": [
        360,
        150
      ],
      "flags": {},
      "order": 14,
      "mode": 0,
      "inputs": [
        {
          "name": "clip",
          "type": "CLIP",
          "link": 204
        },
        {
          "name": "vae",
          "shape": 7,
          "type": "VAE",
          "link": 198
        },
        {
          "name": "image",
          "shape": 7,
          "type": "IMAGE",
          "link": 180
        }
      ],
      "outputs": [
        {
          "name": "CONDITIONING",
          "type": "CONDITIONING",
          "links": [
            210
          ]
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.50",
        "Node name for S&R": "TextEncodeQwenImageEdit",
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "ue_properties": {
          "widget_ue_connectable": {
            "prompt": true
          }
        }
      },
      "widgets_values": [
        ""
      ],
      "color": "#223",
      "bgcolor": "#335"
    },
    {
      "id": 78,
      "type": "LoadImage",
      "pos": [
        -220,
        500
      ],
      "size": [
        274.080078125,
        314.0000305175781
      ],
      "flags": {},
      "order": 6,
      "mode": 0,
      "inputs": [],
      "outputs": [
        {
          "name": "IMAGE",
          "type": "IMAGE",
          "links": [
            177
          ]
        },
        {
          "name": "MASK",
          "type": "MASK",
          "links": null
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.50",
        "Node name for S&R": "LoadImage",
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "ue_properties": {
          "widget_ue_connectable": {
            "image": true,
            "upload": true
          }
        }
      },
      "widgets_values": [
        "pasted/image (8).png",
        "image"
      ]
    },
    {
      "id": 37,
      "type": "UNETLoader",
      "pos": [
        -609.5162963867188,
        30
      ],
      "size": [
        330,
        90
      ],
      "flags": {},
      "order": 7,
      "mode": 0,
      "inputs": [],
      "outputs": [
        {
          "name": "MODEL",
          "type": "MODEL",
          "slot_index": 0,
          "links": []
        }
      ],
      "properties": {
        "cnr_id": "comfy-core",
        "ver": "0.3.48",
        "Node name for S&R": "UNETLoader",
        "models": [
          {
            "name": "qwen_image_edit_fp8_e4m3fn.safetensors",
            "url": "https://huggingface.co/Comfy-Org/Qwen-Image-Edit_ComfyUI/resolve/main/split_files/diffusion_models/qwen_image_edit_fp8_e4m3fn.safetensors",
            "directory": "diffusion_models"
          }
        ],
        "enableTabs": false,
        "tabWidth": 65,
        "tabXOffset": 10,
        "hasSecondTab": false,
        "secondTabText": "Send Back",
        "secondTabOffset": 80,
        "secondTabWidth": 65,
        "widget_ue_connectable": {}
      },
      "widgets_values": [
        "qwen_image_edit_fp8_e4m3fn.safetensors",
        "default"
      ]
    },
    {
      "id": 99,
      "type": "MarkdownNote",
      "pos": [
        -981.4199829101562,
        -18.65259552001953
      ],
      "size": [
        540,
        550
      ],
      "flags": {},
      "order": 8,
      "mode": 0,
      "inputs": [],
      "outputs": [],
      "title": "Model links",
      "properties": {
        "widget_ue_connectable": {}
      },
      "widgets_values": [
        "[Tutorial](https://docs.comfy.org/tutorials/image/qwen/qwen-image-edit) | [教程](https://docs.comfy.org/zh-CN/tutorials/image/qwen/qwen-image-edit)\n\n\n## Model links\n\nYou can find all the models on [Comfy-Org/Qwen-Image_ComfyUI](https://huggingface.co/Comfy-Org/Qwen-Image_ComfyUI/tree/main) and  [Comfy-Org/Qwen-Image-Edit_ComfyUI](https://huggingface.co/Comfy-Org/Qwen-Image-Edit_ComfyUI) \n\n**Diffusion model**\n\n- [qwen_image_edit_fp8_e4m3fn.safetensors](https://huggingface.co/Comfy-Org/Qwen-Image-Edit_ComfyUI/resolve/main/split_files/diffusion_models/qwen_image_edit_fp8_e4m3fn.safetensors)\n\n**LoRA**\n\n- [Qwen-Image-Lightning-4steps-V1.0.safetensors](https://huggingface.co/lightx2v/Qwen-Image-Lightning/resolve/main/Qwen-Image-Lightning-4steps-V1.0.safetensors)\n\n**Text encoder**\n\n- [qwen_2.5_vl_7b_fp8_scaled.safetensors](https://huggingface.co/Comfy-Org/Qwen-Image_ComfyUI/resolve/main/split_files/text_encoders/qwen_2.5_vl_7b_fp8_scaled.safetensors)\n\n**VAE**\n\n- [qwen_image_vae.safetensors](https://huggingface.co/Comfy-Org/Qwen-Image_ComfyUI/resolve/main/split_files/vae/qwen_image_vae.safetensors)\n\nModel Storage Location\n\n```\n📂 ComfyUI/\n├── 📂 models/\n│   ├── 📂 diffusion_models/\n│   │   └── qwen_image_edit_fp8_e4m3fn.safetensors\n│   ├── 📂 loras/\n│   │   └── Qwen-Image-Lightning-4steps-V1.0.safetensors\n│   ├── 📂 vae/\n│   │   └── qwen_image_vae.safetensors\n│   └── 📂 text_encoders/\n│       └── qwen_2.5_vl_7b_fp8_scaled.safetensors\n```\n"
      ],
      "color": "#432",
      "bgcolor": "#653"
    },
    {
      "id": 112,
      "type": "LanPaint_KSampler",
      "pos": [
        626.4457397460938,
        322.53167724609375
      ],
      "size": [
        306.1622619628906,
        469.0702819824219
      ],
      "flags": {},
      "order": 16,
      "mode": 0,
      "inputs": [
        {
          "name": "model",
          "type": "MODEL",
          "link": 208
        },
        {
          "name": "positive",
          "type": "CONDITIONING",
          "link": 209
        },
        {
          "name": "negative",
          "type": "CONDITIONING",
          "link": 210
        },
        {
          "name": "latent_image",
          "type": "LATENT",
          "link": 206
        }
      ],
      "outputs": [
        {
          "name": "LATENT",
          "type": "LATENT",
          "slot_index": 0,
          "links": [
            207
          ]
        }
      ],
      "properties": {
        "aux_id": "scraed/LanPaint",
        "ver": "56bd6c04e89124cd06682b304245d6ddf8b20522",
        "Node name for S&R": "LanPaint_KSampler",
        "cnr_id": "LanPaint"
      },
      "widgets_values": [
        0,
        "fixed",
        4,
        1,
        "euler",
        "simple",
        1,
        5,
        "Image First",
        "LanPaint KSampler. For more info, visit https://github.com/scraed/LanPaint. If you find it useful, please give a star ⭐️!"
      ]
    }
  ],
  "links": [
    [
      141,
      66,
      0,
      75,
      0,
      "MODEL"
    ],
    [
      177,
      78,
      0,
      93,
      0,
      "IMAGE"
    ],
    [
      178,
      93,
      0,
      88,
      0,
      "IMAGE"
    ],
    [
      179,
      93,
      0,
      76,
      2,
      "IMAGE"
    ],
    [
      180,
      93,
      0,
      77,
      2,
      "IMAGE"
    ],
    [
      185,
      89,
      0,
      66,
      0,
      "MODEL"
    ],
    [
      189,
      8,
      0,
      104,
      0,
      "IMAGE"
    ],
    [
      196,
      107,
      0,
      89,
      0,
      "MODEL"
    ],
    [
      197,
      39,
      0,
      76,
      1,
      "VAE"
    ],
    [
      198,
      39,
      0,
      77,
      1,
      "VAE"
    ],
    [
      199,
      39,
      0,
      8,
      1,
      "VAE"
    ],
    [
      200,
      39,
      0,
      88,
      1,
      "VAE"
    ],
    [
      203,
      38,
      0,
      76,
      0,
      "CLIP"
    ],
    [
      204,
      38,
      0,
      77,
      0,
      "CLIP"
    ],
    [
      206,
      88,
      0,
      112,
      3,
      "LATENT"
    ],
    [
      207,
      112,
      0,
      8,
      0,
      "LATENT"
    ],
    [
      208,
      75,
      0,
      112,
      0,
      "MODEL"
    ],
    [
      209,
      76,
      0,
      112,
      1,
      "CONDITIONING"
    ],
    [
      210,
      77,
      0,
      112,
      2,
      "CONDITIONING"
    ]
  ],
  "groups": [
    {
      "id": 1,
      "title": "Step1 - Load models",
      "bounding": [
        -270,
        -40,
        370,
        450
      ],
      "color": "#3f789e",
      "font_size": 24,
      "flags": {}
    },
    {
      "id": 2,
      "title": "Step 2 - Upload image for editing",
      "bounding": [
        -270,
        430,
        370,
        400
      ],
      "color": "#3f789e",
      "font_size": 24,
      "flags": {}
    },
    {
      "id": 3,
      "title": "Step 3 - Prompt",
      "bounding": [
        130,
        130,
        380,
        433.6000061035156
      ],
      "color": "#3f789e",
      "font_size": 24,
      "flags": {}
    }
  ],
  "config": {},
  "extra": {
    "ds": {
      "scale": 0.8390545288824027,
      "offset": [
        416.1423670043787,
        -92.73763538699879
      ]
    },
    "frontendVersion": "1.25.9",
    "ue_links": [],
    "links_added_by_ue": [],
    "VHS_latentpreview": false,
    "VHS_latentpreviewrate": 0,
    "VHS_MetadataImage": true,
    "VHS_KeepIntermediate": true
  },
  "version": 0.4
}
