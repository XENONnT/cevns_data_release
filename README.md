# XENONnT CE$`\nu`$NS Data Release

## Data

The observed data are four-dimensional, with the following observables:

1. Corrected S2 signal amplitude (cS2)
2. Quantile of $`\mathrm{S2}_\mathrm{pre}/\Delta t_\mathrm{pre}`$
3. S1 BDT score
4. S2 BDT score

The post-selection data for each science run (SR) are stored as `.csv` files in the `data` folder.

## Binning

An extended binned likelihood fit is performed. The bin edges for all four dimensions are stored as `.yaml` files in the `binning` folder.

## Templates

The templates that build the four-dimensional likelihood are stored in the `templates` folder. There are four components:

1. **Accidental coincidence (AC):** `templates/sr*/ac/template_XENONnT_sr*_ac_cevns.h5`
2. **Electronic recoil (ER):** `templates/sr*/er/template_XENONnT_sr*_er_cevns.h5`
3. **Neutron:** `templates/sr*/rg/template_XENONnT_sr*_rg_cevns_tly_*_tqy_*.h5`
4. **Monoenergetic nuclear recoil (NR):** `templates/sr*/mono/template_XENONnT_sr*_mono_*_cevns_tly_*_tqy_*.h5`

The monoenergetic NR templates are used to build the solar neutrino and light dark matter templates, given their respective NR spectra. These templates are dimensionless and represent the detection efficiency. All other components are in units of `/t/y`.

The wildcards are defined as follows:

- `sr*` — distinguishes between science runs
- `tly_*` and `tqy_*` — correspond to the nuisance parameters modeling the light yield and charge yield uncertainties
- `mono_*` — indicates the energy of the monoenergetic NR

## Limits

The 90% confidence level upper limits on the light-dark-matter particle–nucleon interaction cross section are stored in the `limits` folder.

## License

The data products in this repository are licensed under the Creative Commons Attribution 4.0 International License (CC-BY-4.0).

If you use this data release, please cite the associated paper and this repository.

## References

- SR0 and SR1 data were used in [Phys. Rev. Lett. 133, 191002](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.133.191002) and [Phys. Rev. Lett. 134, 111802](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.134.111802).
- SR0, SR1, and SR2 data and templates were used in [arXiv:2604.06002](https://arxiv.org/abs/2604.06002).
