# Video-Quality-Analysis-Visualization
This project explores video quality attributes through data visualization, highlighting patterns and insights related to automated video enhancement techniques.
# 📊 Dataset Column Descriptions

This dataset contains information about video sources, their content characteristics, encoding settings, and resulting quality metrics.

---

## 🔹 1. Source Video Information (`s_`)

These columns describe the original input video properties.

- **`s_video_id`**: Unique identifier for each video  
- **`s_width` / `s_height`**: Resolution of the source video (in pixels)  
- **`s_storage_size`**: File size of the source video (bytes)  
- **`s_duration`**: Duration of the video (in seconds)  
- **`s_scan_type`**: Scan format (e.g., progressive or interlaced)

---

## 🔹 2. Content Features (`c_`)

These features capture the visual characteristics and complexity of the video.

### 📌 General Content Metrics
- **`c_content_category`**: Type of content (e.g., sports, animation, movie)  
- **`c_si` (Spatial Information)**: Measures spatial detail/texture complexity  
- **`c_ti` (Temporal Information)**: Measures motion intensity across frames  

### 📌 Scene Change Metrics
- **`c_scene_change_ffmpeg_ratio30/60/90`**: Scene change ratios using FFmpeg at different thresholds  
- **`c_scene_change_py_thresh30/50`**: Scene change detection using Python-based thresholds  

### 📌 Color Histogram Features

#### Mean Brightness Levels
- `c_colorhistogram_mean_dark`  
- `c_colorhistogram_mean_medium_dark`  
- `c_colorhistogram_mean_medium_bright`  
- `c_colorhistogram_mean_bright`  

#### Brightness Variation (Standard Deviation)
- `c_colorhistogram_std_dev_dark`  
- `c_colorhistogram_std_dev_medium_dark`  
- `c_colorhistogram_std_dev_medium_bright`  
- `c_colorhistogram_std_dev_bright`  

#### Temporal Brightness Variation
- `c_colorhistogram_temporal_mean_std_dev_dark`  
- `c_colorhistogram_temporal_mean_std_dev_medium_dark`  
- `c_colorhistogram_temporal_mean_std_dev_medium_bright`  
- `c_colorhistogram_temporal_mean_std_dev_bright`  

---

## 🔹 3. Encoding Parameters (`e_`)

These columns describe how the video was encoded or compressed.

- **`e_crf`**: Constant Rate Factor (lower = higher quality)  
- **`e_width` / `e_height`**: Output resolution  
- **`e_aspect_ratio`**: Display aspect ratio  
- **`e_pixel_aspect_ratio`**: Pixel aspect ratio  
- **`e_codec`**: Video codec used (e.g., H.264, H.265)  
- **`e_codec_profile`**: Codec profile (e.g., baseline, main, high)  
- **`e_codec_level`**: Codec level constraints  
- **`e_framerate`**: Frames per second  
- **`e_gop_size`**: Group of Pictures (GOP) size  
- **`e_b_frame_int`**: Interval or number of B-frames  
- **`e_ref_frame_count`**: Number of reference frames  
- **`e_scan_type`**: Output scan type  
- **`e_bit_depth`**: Bit depth (e.g., 8-bit, 10-bit)  
- **`e_pixel_fmt`**: Pixel format (e.g., yuv420p)

---

## 🔹 4. Target / Quality Metrics (`t_`)

These represent the output performance and perceived quality after encoding.

- **`t_average_bitrate`**: Average bitrate (compression efficiency)  
- **`t_average_vmaf`**: VMAF score (perceptual video quality)  
- **`t_average_vmaf_mobile`**: VMAF score optimized for mobile viewing  
- **`t_average_vmaf_4k`**: VMAF score optimized for 4K displays  
- **`t_average_psnr`**: PSNR (Peak Signal-to-Noise Ratio)

---

## 🧠 Summary

- **`s_`** → Source video properties  
- **`c_`** → Content complexity/features  
- **`e_`** → Encoding settings  
- **`t_`** → Output quality metrics  

---
