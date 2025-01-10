# User guide common info

How to orgenise the Useg guid [check this](https://en.wikipedia.org/wiki/User_guide)

Suggestion of the struct

```text
.
├── ...
├── doc                    # Documentation files
│   ├── algorithm              # Documantation of the algorithms 
│   │   ├── part01              # Part 1 of algorithms
│   │   │   ├── chapter01              # Chapter 1 of Part 1 of algorithms
│   │   │   │   ├── section01              # Section 1 of Chapter 1 of Part 1 of algorithms
│   │   │   │   │   ├── algorithm01              # Algorithm 1 of Section 1 of Chapter 1 of Part 1 of algorithms
│   │   │   │   │   │   ├── point01.md              # Point 1 of Algorithm 1 of Section 1 of Chapter 1 of Part 1 of algorithms
│   │   │   │   │   │   ├── point02.md              # Point 2 of Algorithm 1 of Section 1 of Chapter 1 of Part 1 of algorithms
│   │   │   │   │   │   ├── point03.md              # Point 3 of Algorithm 1 of Section 1 of Chapter 1 of Part 1 of algorithms
│   │   │   │   │   │   └── ...                 # etc.
│   │   │   │   │   ├── algorithm02              # Algorithm 2 of Section 1 of Chapter 1 of Part 1 of algorithms
│   │   │   │   │   │   └── ...                 # etc.
│   │   │   │   ├── section02              # Section 2 of Chapter 1 of Part 1 of algorithms
│   │   │   │   │   └── ...                 # etc.
│   │   │   ├── chapter02              # Chapter 2 of algorithms
│   │   │   │   └── ...                 # etc.
│   │   ├── part02              # Part 2 of algorithms
│   │   │   └── ...                 # etc.
│   │   └── ...                # etc.
│   ├── reference              # Reference Documantation 
│   └── ...                 # etc.
└── ...
```

```text
.
assets/
├── fleet/                     # all ships datasets all ships
|   ├── {numberIMO}_{shipName}    # for ship #1   
|   |   ├── 3d_models/               # 3d models for ship #1  
|   |   |   ├── model_1.obj             # 3d models #1 for ship #1
|   │   |   ├── model_2.obj             # 3d models #2 for ship #1
|   │   |   └── ...                     # etc
|   |   ├── datasets/                # table data for ship #1
|   |   │   ├── csv/                    # csv table data for ship #1
|   |   |   │   ├── data_1.csv             # csv table #1 data for ship #1
|   |   |   │   ├── data_2.csv             # csv table #2 data for ship #1
|   |   |   │   └── ...                    # etc
|   |   |   ├── xls/                    # xls table data for ship #1
|   |   |   │   ├── data_1.xls             # xls table data #1 for ship #1
|   |   |   │   ├── data_2.xls             # xls table data #1 for ship #1
|   |   |   │   └── ...                    # etc
|   |   |   └── ...                     # etc
|   |   └── ...                      # etc
|   ├── {numberIMO}_{shipName}    # for ship #2 
|   |   |   └── ...                  # etc  
|   |   └── ...                  # etc  
|   └── ...                  # etc  
├── images/                   # Images 
|   ├── program_sheets/           # all images of program screen   
|   |   ├── sheet1_mainScreen       # images of main screen 
|   |   |   ├── image_1.png            # images #1 of main screen
│   |   |   ├── image_2.jpeg           # images #2 of main screen
|   |   |   └── ...                    # etc
|   |   ├── sheet2_strength         # images of screen strength 
|   |   |   ├── image_1.png            # images #1 of screen strength
│   |   |   ├── image_2.jpeg           # images #2 of screen strength
|   |   |   └── ...                    # etc
|   |   └── ...
|   └── ...
└── ...
```