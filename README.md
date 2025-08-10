
# Seismic2Attribute

Seismic2Attribute is a Python-based tool designed to compute a wide range of seismic attributes from seismic data. These attributes are essential for subsurface interpretation, fault detection, and geological modeling in the oil and gas industry.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Seismic2Attribute facilitates efficient computation and analysis of seismic attributes from seismic datasets, helping geoscientists extract meaningful information from seismic surveys.

---

## Features

- Compute various seismic attributes such as amplitude, instantaneous phase, coherence, curvature, and more.
- Handles large seismic datasets efficiently.
- Extensible framework allowing easy addition of custom attribute calculations.
- Supports commonly used seismic data formats.

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Amrmoslim/Seismic2Attribute.git
   ```

2. Navigate into the project directory:

   ```bash
   cd Seismic2Attribute
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

### Running the Seismic Attribute Computation

Use the main script to compute seismic attributes from your seismic dataset file:

```bash
python compute_attributes.py --input <input_file> --output <output_directory> [options]
```

- `--input` (required): Path to the input seismic data file (e.g., SEG-Y format `.sgy`).
- `--output` (required): Directory where computed seismic attributes will be saved.
- `[options]` (optional): Additional parameters for customization.

### Example

```bash
python compute_attributes.py --input data/seismic_example.sgy --output results/
```

This command processes `seismic_example.sgy` and saves attribute outputs inside the `results` folder.

### Supported Seismic Attributes

The tool currently supports computation of the following attributes:

- **Amplitude** — Reflects the strength of the seismic signal.
- **Instantaneous Phase** — Represents the phase angle of the seismic wave.
- **Instantaneous Frequency** — Frequency content varying with time.
- **Coherence** — Measures similarity between seismic traces, useful for fault detection.
- **Envelope** — Smooth curve outlining the extremes of the waveform.
- **RMS Amplitude** — Root Mean Square amplitude over a window.
- **Dip** — Angle of inclination of seismic reflectors.
- **Azimuth** — Direction of maximum dip.
- **Spectral Decomposition** — Frequency analysis of seismic data.
- **Variance** — Measure of signal variability.
- **Texture Attributes** — Statistical measures from amplitude patterns.
- **Curvature** — Measures bending or curvature of geological features.
- **Hilbert Transform** — For analytic signal computation.
- **Acoustic Impedance** — Derived rock property related attribute.
- **Instantaneous Q** — Attenuation quality factor estimation.

### Output Files

The output directory will contain files representing computed attributes, possibly in formats such as:

- NumPy arrays (`.npy`)
- CSV or text files
- Other seismic data formats

### Optional Parameters

Some optional flags you might use:

- `--window-size`: Size of the moving window for attribute calculation (default: 5)
- `--attribute-type`: Specify attribute(s) to compute (e.g., amplitude, phase)
- `--verbose`: Enable detailed logging output

### Sample Command with Options

```bash
python compute_attributes.py --input data/seismic_example.sgy --output results/ --window-size 7 --attribute-type amplitude --verbose
```

---

## Contributing

Contributions are welcome! Please fork the repository, create a new branch with your feature or bug fix, and submit a pull request. Make sure to include tests and update documentation where applicable.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Author

Amr Moslim  
[GitHub Profile](https://github.com/Amrmoslim)

---

If you want me to help write examples, tests, or more detailed docs on specific parts, just say the word!
