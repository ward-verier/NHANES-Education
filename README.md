NHANES Education level and Changes in Mortality

This repository contains SAS code and data files used in the analysis of changes in rates of all-cause mortality by education level in the U.S. between participants in NHANES III (1988-1994) and NHANES 2009-2019.  Mortality follow-up through 2019 was provided by the CDC in Linked Mortality files.  All source data are publicly available at www.cdc.gov/nchs/nhanes/Default.aspx and www.cdc.gov/nchs/data-linkage/mortality-public.htm.
	
Data files

nhanes3_domain3.csv                         	 Derived data for NHANES III

nhanes3_domain3_multimp_f3.cvs        			   Multiple imputed data for NHANES III women 60 years and older

nhanes3_domain3_multimp_m3.cvs                 Multiple imputed data for NHANES III men 60 years and older

nhanes0912_domain2.csv                         Derived data for NHANES 2009-2012

nhanes0912_domain2_multimp_f3.csv              Multiple imputed data for NHANES 2009-2012 women 60 years and older

nhanes0912_domain2_multimp_m3.csv              Multiple imputed data for NHANES 2009-2012 men 60 years and older



SAS Program files and work flow

1.  SAS_ReadinProgramAllSurveys.txt		Loads formats for mortality data
2.  datacreate.txt
3.  descriptive_raw_imputed.txt
4.  agebyedlevel_m60_freq.txt and agebyedlevel_f60_freq.txt		(2 files) provide disease frequencies in NHANES 2009-2012 in men and women, for use as sampling frequencies in NHANES III
5.  prevalence_m60_ami_multimp2.txt to prevalence_f60_waist_multimp2.txt	(24 files)  create 500 random samples of NHANES III participants (by sex) having same prevalence of corresponding disease as in NHANES 2009-2012, computes 500 adjusted odds ratios for education level
6.  cox_m60_bmi_multimp2.txt to cox_f60_multimp2.txt   (24 files)  computes adjusted hazard ratios for education level on above generated 500 random samples per disease and sex group
7.  m3_f3_or_interactions_n0912.txt		logistic models testing effect modification by disease between NHANES III and NHANES 2009-2012
8.  m3_f3_hr_interactions_n0912.txt		Cox models testing effect modification by disease between NHANES III and NHANES 2009-2012 
