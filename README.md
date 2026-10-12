# GenAI exposure scores for Polish six-digit occupations (ILO–NASK Global AI Exposure Index, 2025)

Task-level generative AI (GenAI) exposure scores for 2,541 occupations of Poland's national classification of occupations (KZiS, six digits), with task text in Polish and English, scored with the same method as the ISCO-08 index of ILO Working Paper 140. Scores run from 0 (the task cannot be performed by current GenAI) to 1 (it could be performed entirely by GenAI). Exposure means technical potential. It is not a prediction of job loss.

Interactive explorer: https://pgmyrek.github.io/ai-exposure-explorer/ (switch to the Poland 6-digit level).

## Files

- `POLAND_FINAL_6digit_scores.xlsx`: scores by task, with Polish and English task text, the 2025 score and the model justification
- `ISCO_mapping.csv`: mapping of ISCO-08 four-digit occupations to their parent groups
- `Poland_6digit_tree_plot_EN.xlsx`, `output_data_EN.json`, `transformation_EN.ipynb`: data and code behind the tree viewer
- `index.html`, `script.js`: the tree viewer
- `Gmyrek et al. 2025, ILO Working Paper 140_web.pdf`: the working paper

Companion data for ISCO-08: https://github.com/pgmyrek/2025_GenAI_scores_ISCO08

## Licence and citation

This work is licensed under the Creative Commons Attribution 4.0 International licence (CC BY 4.0). See [LICENSE](LICENSE) and https://creativecommons.org/licenses/by/4.0/. You may reuse, share (copy and redistribute) and adapt (remix, transform and build upon) the material as detailed in the licence. You must clearly credit the ILO as the source of the material and indicate if changes were made.

**Attribution.** Cite the work as follows:

Gmyrek, P., Berg, J., Kamiński, K., Konopczyński, F., Ładna, A., Nafradi, B., Rosłaniec, K., Troszyński, M. 2025. *Generative AI and Jobs: A Refined Global Index of Occupational Exposure*. ILO Working Paper 140. Geneva: International Labour Office. © ILO. https://doi.org/10.54394/HETP0387

**Translations.** If you translate this work, add the following disclaimer along with the attribution: *This is a translation of a copyrighted work of the International Labour Organization (ILO). This translation has not been prepared, reviewed or endorsed by the ILO and should not be considered an official ILO translation. The ILO disclaims all responsibility for its content and accuracy. Responsibility rests solely with the author(s) of the translation.*

**Adaptations.** If you adapt this work, add the following disclaimer along with the attribution: *This is an adaptation of a copyrighted work of the International Labour Organization (ILO). This adaptation has not been prepared, reviewed or endorsed by the ILO and should not be considered an official ILO adaptation. The ILO disclaims all responsibility for its content and accuracy. Responsibility rests solely with the author(s) of the adaptation.*

**Emblem and logo.** Use of the emblem, name and logo of the ILO is not permitted in connection with translations, adaptations or other derivative works.

**Third-party materials.** This Creative Commons licence does not apply to non-ILO copyright materials. If material is attributed to a third party, the user of such material is solely responsible for clearing the rights with the rights holder and for any claims of infringement.

**Polish classification.** The occupation titles and task descriptions come from Poland's national classification of occupations (KZiS), maintained by the Ministry of Family, Labour and Social Policy. They are not ILO material, and the Creative Commons licence above covers the ILO scores and other ILO-authored content. If you reuse the classification text itself, check the terms of its publisher.

**Disputes.** Any dispute arising under this licence that cannot be settled amicably shall be referred to arbitration in accordance with the Arbitration Rules of the United Nations Commission on International Trade Law (UNCITRAL). The parties shall be bound by any arbitration award rendered as a result of such arbitration as the final adjudication of such a dispute.

**Disclaimer.** The designations employed and the presentation of material do not imply the expression of any opinion whatsoever on the part of the ILO concerning the legal status of any country, area or territory or of its authorities, or concerning the delimitation of its frontiers or boundaries. The opinions and views expressed are those of the author(s) and do not necessarily reflect the opinions, views or policies of the ILO. Reference to names of firms and commercial products and processes does not imply their endorsement by the ILO.

For rights and licensing, contact rights@ilo.org. Comments on the working paper are welcome at gmyrek@ilo.org.
