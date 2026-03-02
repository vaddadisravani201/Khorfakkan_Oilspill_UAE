This project analyzes a reported oil spill near Khor Fakkan, UAE, in May 2025 using Sentinel-1 SAR imagery in Google Earth Engine. SAR-based thresholding techniques are applied to VV polarization data to identify potential oil slick areas during a two-week monitoring window.


📍Study Area: Khor Fakkan, UAE
This analysis focuses on coastal waters near Khor Fakkan, located along the Gulf of Oman on the eastern coast of the United Arab Emirates.
The selected coordinates (56.36°E, 25.34°N) are near Al Zubarah Beach.

🛢️ Oil Spill Event – May 2025
In mid-May 2025 (around May 18–20), reports emerged of an oil slick detected off the coast of Khor Fakkan in the Emirate of Sharjah, United Arab Emirates.

Key reported details:

Oil contamination was observed along sections of the coastline.

Cleanup operations were initiated by local authorities.

The source of the spill was investigated, with attention given to maritime traffic in the Gulf of Oman.

Satellite monitoring was used to assess the spatial extent of the slick.

Because oil on water dampens capillary waves, it appears as dark patches (low backscatter) in Synthetic Aperture Radar (SAR) imagery. This makes Sentinel-1 SAR data especially suitable for detecting marine oil spills regardless of cloud cover.

🛰️ Satellite Data Used

This project uses imagery from:

European Space Agency

Sentinel-1

Dataset: COPERNICUS/S1_GRD

Mode: IW (Interferometric Wide Swath)

Polarization: VV

Orbit: Descending pass

Date Range: May 14–26, 2025

The 2-week time window captures imagery:

Before the reported spill

During peak visibility

After initial dispersion

🧠 Detection Method

The workflow:

Filter Sentinel-1 GRD imagery over the study area.

Select VV polarization.

Compute a median composite to reduce speckle noise.

Apply a backscatter threshold (VV < -22 dB) to detect dark pixels.

Visualize potential oil slick areas in cyan.

Oil slicks reduce radar backscatter because they smooth the sea surface, producing darker signatures in SAR imagery.

<img width="1906" height="751" alt="image" src="https://github.com/user-attachments/assets/a60d087d-6300-4929-b8a8-874f45593cf2" />
