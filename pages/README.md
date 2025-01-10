## About

The Intern Sleep and Patient Safety Study (ISAPS), as part of the Harvard Work Hours, Health and Safety Study from July 2002 to June 2003, was designed to quantify work hours, sleep, and the rates of medical errors among interns working in critical care units. The objectives of the study were to quantify work hours and sleep in interns during a traditional schedule, to compare subjective reports of work hours and sleep with simultaneous, independent, objective measures, and to measure the effect of an intervention designed to eliminate extended work shifts on physicians' work hours, sleep, and attentional failures. Using a within-subjects design, 20 individuals who had accepted a position in the postgraduate internal medicine residency training program (PGY-1) at the Brigham and Women’s Hospital were each studied during two three-week critical care rotations while working the following two schedules: 1) a traditional schedule with extended duration work shifts of ~30 consecutive hours every other shift; 2) an intervention schedule designed to eliminate extended duration work shifts (to a maximum of 16 consecutive hours). 

The NSRR ISAPS dataset includes data from 34 individuals, who completed daily work logs, sleep logs, and underwent continuous ambulatory polysomnographic monitoring while at work or at home between 2002 and 2003. 

## Methods

### Coverage schedules

Using a within-subjects design, 20 interns were studied during two three-week rotations in the medical intensive care unit (MICU) and coronary care unit (CCU) while following a traditional schedule with extended work shifts of 30 consecutive hours scheduled every other shift and an intervention schedule in which work shifts were a maximum of 16 consecutive hours scheduled. The remaining four subjects were studied while they followed a pilot intervention schedule that was discontinued after the first MICU rotation (data not included). During the traditional schedule, three interns provided continuous coverage on a three-day cycle, officially consisting of a day shift (approximately 7 a.m. to 3 p.m.) on day 1 followed by an extended work shift from 7 a.m. on day 2 to noon on day 3, although in actual practice, interns often worked beyond those hours.

### PSG collection

Continuous ambulatory polysomnographic (Vitaport-2/3, TEMEC Instruments B.V., The Netherlands) monitoring was conducted at work or at home in order to capture one full 3- or 4-day rotation per subject per week during the traditional and intervention rotations, respectively.

PSG recordings consisted of a simultaneous electroencephalogram (EEG; C3,C4,F3,F4 referenced to contralateral mastoid [A1 or A2] when at home; Fz,Cz,Pz,Oz referenced to linked mastoid [Ax] while working in the hospital), electrooculogram (EOG), and electrocardiogram (ECG). Electromyograms (EMG) were recorded during sleep at home. The signals were digitized (sampling rate 256 Hz for EEG/EMG/ECG; 128 Hz for EOG), band-pass filtered (EEG,EOG: 0.16-35 Hz; ECG: 1-70 Hz; EMG: 10.6-50 Hz), and stored on a Flash RAM card. Electrodes were applied and removed by a technician trained in polysomnography in the General Clinical Research Center, although interns were instructed to apply the mentalis/sub-mentalis EMG electrodes before all sleep episodes at home. Interns were provided with a 24-hour pager number to call in case of technical difficulties or accidental electrode removal.

## Data de-identification

All personally identifiable information (PII) has been removed from the data files by the NSRR team.

## Data overview

### Covariate/phenotype datasets (CSV)

The [covariate dataset files](:files_path:/datasets) (**isaps-dataset-0.1.0.csv** and **isaps-harmonized-dataset-0.1.0.csv**) contain 34 rows each. The first column ([nsrrid](:variables_path:/nsrrid)) is the unique ISAPS subject identifier that can be linked with PSG signal filenames. 

The dataset columns are described in the accompanying data dictionary files. The **variables** data dictionary file includes column names (id), labels (display names), descriptions, and other metadata. Categorical variables also include an associated "domain" (e.g., 0=Male, 1=Female), which are described in the **domains** data dictionary file. 

The history of the covariate dataset and data dictionary files have been tracked on GitHub (https://github.com/nsrr/isaps-data-dictionary). 

The harmonized-dataset contains many of the most frequently used demographic and sleep variables. These variables were curated by the NSRR team. Key variables include:

  <table>
    <tr><td><b>Variable</b></td><td><b>Label</b></td></tr>
    <tr><td><a href=":variables_path:/nsrr_age">nsrr_age</a></td><td>Subject age</td></tr>
    <tr><td><a href=":variables_path:/nsrr_sex">nsrr_sex</a></td><td>Subject sex</td></tr> 
  </table>

### PSG signal files (EDF/XML)

[Raw signal data](:files_path:/original) are shared as EDF files using the European Data Format (https://www.edfplus.info/). 

Each folder contains data from a single subject. Dates were removed from the EDF headers. Filenames are formatted as such: SubjectID_DaysFromFirstDate_FileCounterWithinDay_ScheduleInfo.

  <table>
    <tr><td><b>Filename portion</b></td><td><b>Description</b></td></tr>
    <tr><td>SubjectID</td><td>Subject identifier ([filename_id](:variables_path:/filename_id))</td></tr>
    <tr><td>DaysFromFirstDate</td><td>The number of calendar days from the first EDF date for the given subject </td></tr>
    <tr><td>FileCounterWithinDay</td><td>An incrementing number for EDF files with start times on the same calendar day </td></tr>  
    <tr><td>ScheduleInfo</td><td>B - Block 1, 2 or 3 - denotes the 2-3 day period of ambulatory in each of the three weeks of study <br> SP - Sleep Period within Block <br> WP - Wake Period within Block <br> PT - part of Wake Period - may have required multiple separate recordings to capture <br> OC - On-call, this is the control condition where interns were scheduled to a Q3 schedule - an on-call 24+ hour shift every three days <br>  IV - Intervention, this is the intervention condition where the 24+hour shift was broken into two shorter shifts with a break in between </td></tr> 
  </table>

## Access and usage restrictions

The ISAPS dataset is only available for non-commercial use.

## Citation and acknowledgement

When using this dataset, users must cite the following:

> [Zhang GQ, Cui L, Mueller R, Tao S, Kim M, Rueschman M, Mariani S, Mobley D, Redline S. The National Sleep Research Resource: towards a sleep data commons. J Am Med Inform Assoc. 2018 Oct 1;25(10):1351-1358. doi: 10.1093/jamia/ocy064. PMID: 29860441; PMCID: PMC6188513.](https://pubmed.ncbi.nlm.nih.gov/29860441/)
> 
> [Lockley SW, Cronin JW, Evans EE, Cade BE, Lee CJ, Landrigan CP, Rothschild JM, Katz JT, Lilly CM, Stone PH, Aeschbach D, Czeisler CA; Harvard Work Hours, Health and Safety Group. Effect of reducing interns' weekly work hours on sleep and attentional failures. N Engl J Med. 2004 Oct 28;351(18):1829-37. doi: 10.1056/NEJMoa041404. PMID: 15509816.](https://pubmed.ncbi.nlm.nih.gov/15509816/)

Users must include the following text in any Acknowledgements:

> The National Sleep Research Resource was supported by the U.S. National Institutes of Health, National Heart Lung and Blood Institute (R24 HL114473, 75N92019R002).

## Changelog

*January 2025*

- Make ISAPS dataset available for data requests

## References

-	ISAPS GitHub Documentation: https://github.com/nsrr/isaps-documentation
-	ISAPS GitHub Data Dictionary: https://github.com/nsrr/isaps-data-dictionary

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.
