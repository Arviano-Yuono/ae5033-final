This task is done as the final module of AE5033 Flight Simulator Technology course material. The task description can be seen in `task.pdf` and the raw dataset was obtained through XPlane10 simulation of 3 groups stored in `data/data.txt`.

# Setup
It is recommended to use `uv` for this project. To install `uv` using `pip`, you can simply use,
`pip install uv`

Now, simply clone the repo and sync the venv with `uv`

```bash
git clone https://github.com/Arviano-Yuono/ae5033-final.git

cd ae5033-final

uv sync
```

# Results Summary
This discussion is baed on the table and figures presented in `preprocess-analysis.ipynb` notebook.

- Our file contains 12 raw mission segments. Raw mission 1 is setup/aborted data, and raw mission 2 is excluded as a control-familiarization run.
- The final report set therefore contains 10 repeatable takeoff maneuvers at the 50 ft target.
- Differences between maneuvers can come from rotation timing, elevator pull rate, how tightly 10 deg pitch was held, runway alignment, airspeed at rotation, and the exact moment the simulator reset/log started.
- For an Aircraft Flight Manual value, do not use the minimum distance. If every run followed the stated procedure, use the maximum measured distance or a rounded value above it. If a run is documented as nonrepresentative, exclude it transparently and use the maximum of the remaining valid runs plus a conservative margin.
- Pilot procedure wording can be: set takeoff flap configuration, hold aircraft aligned on runway threshold, apply full throttle, maintain runway centerline, rotate at the selected reference speed with a smooth pull to about 10 deg pitch, hold the target pitch through the selected obstacle height, then accelerate/climb normally.
