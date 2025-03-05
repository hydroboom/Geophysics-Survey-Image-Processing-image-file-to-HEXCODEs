# Geophysics-Survey-Image-Processing-image-file-to-HEXCODEs

## 🔍 About This Project
This project automates the process of extracting resistivity data from **terrameter reading images**, where the **raw numerical data is unavailable**. Instead of **manually identifying colours** and entering resistivity values into GIS, this script:
- **Overlays a grid on the image** and extracts the most frequent color per cell.
- **Converts colors to HEX values** for further processing.
- **Outputs structured data (CSV & Excel heatmap)** for analysis.
- **Prepares for GIS integration**, where HEX colors will be replaced with resistivity values and georeferenced.

The uploaded files are inclusive of the **input image file** as sample along with the **python script** written in Jupyter Notebook.

This is the **first step** in streamlining **geophysical data analysis**, ultimately generating **depth-based resistivity rasters** in GIS.

---

## 🛠 Modules Used & Their Purpose
This project relies on some specialized Python modules:

1. **[`openpyxl`](https://openpyxl.readthedocs.io/en/stable/)**  
   - Used for **creating an Excel-based heatmap** of the extracted resistivity values.
   - The **`PatternFill`** function applies colours to Excel cells based on HEX values.

2. **[`Pillow (PIL)`](https://pillow.readthedocs.io/en/stable/)**  
   - Used for **image processing and colour extraction**.
   - Loads the **terrameter image** and converts it to **RGB format** for analysis.

3. **[`collections.Counter`](https://docs.python.org/3/library/collections.html#collections.Counter)**  
   - Helps find the **most frequent colour** in each grid cell.
   - Ensures that the extracted colour represents the dominant resistivity reading.

These modules allow us to **efficiently process images, extract meaningful data, and visualize results**.

---

## 🚀 How It Works
1. 📥 **Input**: An image of terrameter readings (from slides, reports, etc.).
2. 🖼 **Processing**: 
   - Divides the image into a **structured grid**.
   - Identifies the **most common color** in each grid cell.
   - Converts colors to **HEX format**.
3. 📊 **Output**: 
   - A **CSV file** mapping Grid_X, Grid_Z, and HEX colors.
   - A **color-coded Excel heatmap** for visualization.
4. 🌍 **Next Steps**: 
   - Replace HEX colors with **resistivity values** using a reference chart.
   - Georeference the extracted data in **GIS** for spatial analysis.

---

## 📖 References & Learning More
- **Python Imaging Library (Pillow)**: [Pillow Documentation](https://pillow.readthedocs.io/en/stable/)  
- **Excel Automation (openpyxl)**: [openpyxl Documentation](https://openpyxl.readthedocs.io/en/stable/)  
- **Efficient Data Counting (collections.Counter)**: [Python Collections Documentation](https://docs.python.org/3/library/collections.html#collections.Counter)

---

## 🤝 Contributions & Feedback
This project is a work in progress! Feel free to **contribute, suggest improvements, or fork the repo**. 🚀
