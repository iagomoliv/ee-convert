# ee-convert
Convert PNG and JPG images to GeoTIFF format, optimized for integration with Google Earth Engine.

## Installation

### Clone the repository
```bash
git clone https://github.com/iagomoliv/ee-convert.git
cd ee-convert
```

### Setup Python environment

Creating a virtual environment to keep the project's dependencies separate from your global Python libraries is recommended. You can do this by running:

```bash
python -m venv venv
source venv/bin/activate
```

### Install dependencies

Within the virtual environment, install the project's dependencies with the following command:

```bash
pip install -r requirements.txt
```

### Prepare images

Copy the images you want to convert into the `input` folder.

## Usage

After installation, you can run the project with:

```bash
python main.py
```

Once `main.py` is executed, the converted images will be available in the `output` folder.

## Uploading into Google Earth Engine

After converting your images, you can upload them as assets into Google Earth Engine.

1. Go to the GEE Code Editor.
2. Click on the `Assets` tab.
3. Select `New` and then `GeoTIFF` under **Image Upload**.
4. Click the **Select** button to choose the converted GeoTIFF files from the `output` folder.
5. Fill out the necessary metadata for your image and click `Upload`.

**Note on transparent backgrounds**

If your original PNG images have a transparent background, select the "Use last band as alpha band" option in "Masking mode" during uploading. This step is crucial to handle the transparency in the images correctly.