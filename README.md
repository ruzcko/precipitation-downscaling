# precipitation-downscaling

A hands-on notebook for AI precipitation downscaling, made for beginners. You run [spateGAN-ERA5](https://github.com/LGlawion/spateGAN_ERA5) on Typhoon Nando (Ragasa), 20 to 24 September 2025, over northern Luzon. It turns ERA5 rain (25 km squares, every hour) into 2 km squares every 10 minutes, then shows the two side by side with a slider and saves a GIF.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ruzcko/precipitation-downscaling/blob/main/downscale_nando.ipynb)

## Run it

1. Click **Open in Colab** above. A free Google account is enough.
2. Optional: choose *Runtime > Change runtime type > T4 GPU* for a faster run. The free CPU also works.
3. Run the six steps from top to bottom. The downscaling step takes about a minute on a GPU and several minutes on a CPU.
4. Pick another area or seed in Step 3 and run Steps 4 to 6 again.

To keep your changes, use *File > Save a copy in Drive*.

## Files

| File | What it does |
|---|---|
| `downscale_nando.ipynb` | The hands-on notebook. |
| `prep_nando_era5.ipynb` | Cuts the ERA5 rain for the case from Google's public ARCO-ERA5 copy and saves `data/nando_era5.nc`. Run it once in Colab to rebuild the data file or to make one for another storm. |
| `data/nando_era5.nc` | Hourly ERA5 convective and large-scale precipitation, 8–26°N, 112–130°E, 20–24 Sep 2025. |

## Credits

- Model: Glawion et al. (2025), "Global spatio-temporal ERA5 precipitation downscaling to km and sub-hourly scale using generative AI", *npj Climate and Atmospheric Science*. Code: [LGlawion/spateGAN_ERA5](https://github.com/LGlawion/spateGAN_ERA5) (MIT).
- Data: ERA5, Copernicus Climate Change Service (C3S), via [Google ARCO-ERA5](https://github.com/google-research/arco-era5). Contains modified Copernicus Climate Change Service information 2025.

## License

The notebooks are MIT licensed. See [LICENSE](LICENSE).
