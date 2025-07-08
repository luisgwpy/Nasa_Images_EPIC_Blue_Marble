# 🌍 NASA EPIC Image Downloader & Video Maker

This project automates the process of downloading high-resolution Earth images from NASA’s [EPIC (Earth Polychromatic Imaging Camera)](https://epic.gsfc.nasa.gov/about/api) API and compiles them into a time-lapse video.

---

## 🚀 Features

- ✅ Retrieve available image dates from NASA EPIC API
- ✅ Fetch and format image download URLs from metadata
- ✅ Download EPIC images asynchronously (10 at a time)
- ✅ Generate a time-lapse `.mp4` video from the downloaded images
- ✅ Overlay timestamps on video frames
- ✅ Handles missing images gracefully

---

## 🛰️ Source: EPIC Daily “Blue Marble” API

NASA's EPIC camera captures full-color images of Earth from the DSCOVR satellite, located at the Lagrange Point 1 (L1). This tool uses the [Natural color](https://epic.gsfc.nasa.gov/about/api) image archive.

🔗 **API Documentation:**  
[https://epic.gsfc.nasa.gov/about/api](https://epic.gsfc.nasa.gov/about/api)

---

## 📥 Image Downloader

**API_NASA_BLUE_MARBLE.ipynb**

The downloader fetches metadata and builds a dataframe of image URLs. It then downloads the images concurrently and saves them using their timestamp-based identifiers.

### 🧩 Example Output Format:

Identifier: 20151031074844
Filename: 20151031074844.png
URL: https://epic.gsfc.nasa.gov/archive/natural/2015/10/31/png/epic_1b_20151031074844.png

### 🖼️ Sample Image:

![EPIC Sample Frame](https://epic.gsfc.nasa.gov/archive/natural/2015/10/31/png/epic_1b_20151031074844.png)

---

## 🎞️ Video Maker

**Video_Eath.ipynb**

The `video_maker()` function creates a video from downloaded images, adding a timestamp overlay on each frame.

### 🔧 Usage:
```python
video_maker(
    output_video="earth_timelapse.mp4",
    duration=10,
    list_images=["20151031074844", "20151031075444", ...],
    PATH_IMAGE="path/to/images"
)
```

---

## 📊 Results

After running this project over the full dataset from **2015 to 2025**, the following results were obtained:

- 📸 **Total images downloaded:** 47,678  
- 🗓️ **Date range:** 2015 – 2025  
- 💾 **Storage used:** 128 GB of PNG images  
- 🎬 **Time-lapse video generated** from the full archive of EPIC natural color images, 9.3 GB of Video

### 🌐 Simulated Video Links

- ▶️ **YouTube Video:** [Data Data no Mi](add_video)  
- 📱 **Instagram Reel:** [@Luis_gwpy](add_video)


