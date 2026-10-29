# precipitation-downscaling

A hands-on notebook for AI precipitation downscaling, made for beginners. You run [spateGAN-ERA5](https://github.com/LGlawion/spateGAN_ERA5) on one of three typhoons that hit the Philippines: Nando (Ragasa, September 2025) over the Ilocos coast, Kristine (Trami, October 2024) over Bicol, and Tino (Kalmaegi, November 2025) over Cebu. It turns ERA5 rain (25 km squares, every hour) into 2 km squares every 10 minutes, then shows the two side by side with a slider and saves a GIF.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ruzcko/precipitation-downscaling/blob/main/downscale_typhoons.ipynb)

## Run it

1. Click **Open in Colab** above. A free Google account is enough.
2. Optional: choose *Runtime > Change runtime type > T4 GPU* for a faster run. The free CPU also works.
3. Run the five steps from top to bottom. The downscaling step takes about a minute on a GPU and several minutes on a CPU.
4. Pick another typhoon or seed in Step 2 and run Steps 3 to 5 again.

To keep your changes, use *File > Save a copy in Drive*.

## Keep your work on GitHub (optional)

GitHub is not needed to run the notebook. If you have an account, you can:

- **Star this repo** (top right) so you can find it again.
- **Save your run** to your own repository: in Colab, choose *File > Save a copy in GitHub*. The repository must exist first; make one at [github.com/new](https://github.com/new) with *Add a README file* ticked.
- **Add your GIF** to that repository with *Add file > Upload files*.

The last section of the notebook walks through these steps, including making an account.

## Files

| File | What it does |
|---|---|
| `downscale_typhoons.ipynb` | The hands-on notebook. |
| `prep_era5.ipynb` | Cuts the ERA5 rain for each typhoon from Google's public ARCO-ERA5 copy. Run it once in Colab to rebuild the data files or to add another typhoon. |
| `data/*_era5.nc` | Hourly ERA5 convective and large-scale precipitation for each typhoon, four days each. |

## Credits

- Model: Glawion et al. (2025), "Global spatio-temporal ERA5 precipitation downscaling to km and sub-hourly scale using generative AI", *npj Climate and Atmospheric Science*. Code: [LGlawion/spateGAN_ERA5](https://github.com/LGlawion/spateGAN_ERA5) (MIT).
- Data: ERA5, Copernicus Climate Change Service (C3S), via [Google ARCO-ERA5](https://github.com/google-research/arco-era5). Contains modified Copernicus Climate Change Service information 2024–2025.

## License

The notebooks are MIT licensed. See [LICENSE](LICENSE).
