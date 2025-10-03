CO2Sys Excel Version History


         Previous versions (2007):  CO2sys_macro_PC.xls   and CO2sys_macro_MAC.xls
               . Two separate files for PC and MAC versions. 
         
         Version 1.0 (10 Octobre 2011):  CO2Sys_2011.xls
               . Combined PC and MAC versions of previous macro into one file working on both platforms. 
         
         Version 2.0 (19 July 2012):  CO2Sys_2011.xls
               . New R formulation from NIST Physical Reference Data (http://physics.nist.gov/cgi-bin/cuu/Value?r) 
                        Difference with old formulation  is not numerically significant. 
               . Matched formulation of Uppstrom's Total Boron with Matlab program (same numerical results). 
               . Added option of Total Boron from Lee et al., 2010 
               . Added a few formulations for K1, K2: 
                         - Cai and Wang, 1998 
                         - Lueker et al., 2000 
                         - Mojica Prieto et al., 2002 
                         - Millero et al., 2002 
                         - Millero et al., 2006 
                         - Millero, 2010 
               . Updated the INFO section 
               . Added the Macro Version History option in INFO Sheet. 
               . Version number is displayed in cell B2 when the About this Macro option in INFO Sheet is selected. 
         
         Version 2.1 (18 September 2012):  CO2Sys_v2.1.xls
               . Corrected an error in the code which affected the results when the constants of 'Millero et. al., 2002' 
                         and 'Millero, 2010' were selected. 
               . References to  'Cai and Wang, 2008' have been corrected to 'Cai and Wang, 1998' 
               . Incorporated version number in the name of the file and removed it from the "INFO" sheet (see v.2.0)

         Special Version 2.1 (03 May 2015):  CO2Sys_v2.1 NH3-H2S
               . Added option to include NH3 and H2S in the calculations of Alkalinity.
			- NH3 constants were taken from the [Clegg Whitfield 1995   Geochimica et Cosmochimica Acta, Vol. 59, No. 12. pp. 2403-2421] paper referenced in the Bell et al (2007) article. Their values are valid from S=[0-40] and T=[-2-40 oC].
			- H2S constants were taken from Millero et. al. (1988)  Limnol. Oceanogr. 33,269-274 and are valid from S=[0-40] and T=[0-35 oC]
 
			- Pressure correction taken from Millero (1983) “Influence of Pressure on Chemical Processes in the Sea” (the Millero 1995 had typos)   

               . Bug fix: added code to prevent calculation of pH (fromTATC or fromTAfCO2) from getting stuck in infinite loop of alternatively negative and positive delta pHs.(taken from version 2.3 on 14 November 2016)
               . Bug fix: Corrected handling of -999 in data. would skip line at first encountered -999 in CO2 parameter. Would also not handle -999 in output conditions. (taken from version 2.3 on 11/18/2016)
	       . Bug fix: KH2S from Yao Millero was actually given on Total Scale and not Seawater scale. Corrected in the code. Also cleaned up the code. (12/14/2016)
	       . Issue fix: Added a check to stop iterations of pH estimation after 10,000 loops and flag data (pH did not converge). (12/14/2016)
	       . Issue fix: data flag is now in proper column and text color is red when flagged (12/14/2016)

         Version 2.2 (27 October 2015): CO2sys_v2.2xls - based on regular v2.1 (no H2S-NH3)

               . Added the choice of 'Perez and Fraga, 1987' for KF
               . Added the 'SubFlags' and 'Red data rows': 
                        If Pressure, Phosphate or Silica is '-999', calculations will be performed with  0 instead of -999
                        and the resulting row of data will be colored in red. The 'SubFlag' column at the end will state the reason.


         Version 2.3 (14 December 2016): CO2sys_v2.3xls - based on regular v2.2 (no H2S-NH3)

               . Corrected output format of results
               . Bug fix: added code to prevent calculation of pH (fromTATC or fromTAfCO2) from getting stuck in infinite loop of alternatively negative and positive delta pHs.
               . Bug fix: Corrected handling of -999 in data. would skip line at first encountered -999 in CO2 parameter. Would also not handle -999 in output conditions. (11/18/2016)
               . Bug fix: Corrected coloring of problematic line in red and expanded "results" range to clear to include flag in last column. (11/18/2016)
	       . Issue fix: Added a check to stop iterations of pH estimation after 10,000 loops and flag data (pH did not converge). (12/14/2016)
	       . Issue fix: data flag is now in proper column and text color is red when flagged (12/14/2016)
               . found numvar misspelled as “numbar”. Doesn’t seem to create issue. Fixed anyway (05/13/2019)

         Special Version 2.3 (14 December 2016): CO2sys_v2.3  NH3-H2Sxls - based on regular v2.3 (no H2S-NH3) dated (12/14/2016)
	  
	   . See changes made to version 2.3 dated on 12/14/2016 and before, as well as those made to Special version 2.1 (12/14/2016) (called v2.4 on GitHub)
               . found numvar misspelled as “numbar”. Doesn’t seem to create issue. Fixed anyway (05/13/2019)

        
         Version 3.0 (15 June 2019): CO2sys_v3.0.xls
               . Incorporated a special version including NH3 and H2S in the calculations of Alkalinity (see Xu et al. Mar. Chem. 195 (2017) pp.90-93) 
               . Added ""Carbonate Ions"" as an input carbonate parameter (06/12/2019)
               . Modified way to select carbonate parameters to use for the calculations. User has to select headers which will be highlighted in green. They will also be highlighted in the ""input"" section. (06/12/2019)
               . Cleaned the code

         Version 3.0 with error propagation (05 May 2020): CO2sys_v3.0_Orr.xlsm - based on Special v2.3

             . Updated the info about the macro and the NH4-H2S constants (06/07/2019)
	     . Suppressed screen updating when selecting cells on INFO and INPUT sheets (06/07/2019)
       	     . Incorporated a special version including NH3 and H2S in the calculations of Alkalinity (see Xu et al. Mar. Chem. 195 (2017) pp.90-93)
       	     . Added ""Carbonate Ions"" as an input carbonate parameter (06/12/2019)
             . Modified way to select carbonate parameters to use for the calculations. User has to select headers which will be highlighted in green. They will also be highlighted in the ""input"" section. (06/12/2019)"
             . Cleaned the code
  	     . Bug fix: affected calculation of KF of 'Perez and Fraga, 1987' (lnKF was spelled InKF instead- first letter was a cap “i” instead of an “L”).(07/18/2019)
	     . Added Peng’s correction of TA for case of input TA, Carbonate.(07/18/2019)
	     . Clearing Results now also clears pH Scale and Constants used. (07/22/2019)
             . Issue fix: When selecting Peng or GEOSECS K1,K2 options, NBS pH Scale is automatically selected. (01/28/2020)
             . Added Error Propagation calculations of Orr et al. (2019)
             . Added Error Propagation code from Orr's version. (04/29/2020)
             . Added calculation and output of pHs on all scales and all pKs for in and out conditions on separate sheet. (04/29/2020)
             . Issues fix: wrong R and wrong TC used in Revelle Factor calculation. (06/22/2020)
             . Added the Waters and Millero, 2013 and Sulpis et al. 2020 constants to match the Matlab and Python versions. (06/22/2020)
             . Updated R formulation from ""NIST Physical Reference Data (http://physics.nist.gov/cgi-bin/cuu/Value?r)""
                     R is now a Public Constant = 83.14462618 in the program. It agrees with the value used in the Matlab and Python versions.
                     Difference with old formulation is not numerically significant.
 	     . In calculations involving pH and Alkalinity, Hfree is now calculated differently depending on pH scale (Total Scale was assumed before) (04/03/2021)
	     . Uncertainties of parameters can either be input as one for all points on the INPUT sheet, or one for each point on the ERROR sheet.
    	        Selection of input is done on the INPUT sheet. (05/05/2021)
	     . pH Scale and Constants used (column R in DATA sheet) are refreshed when activating the DATA sheet. (02/05/2021)
             . Parameters used for the calculation of data and errors have their header highlighted in green on the DATA and ERROR sheet (05/05/2021)
	     . Case structure for selection of K1,K2 set has been modified. Only special cases (GEOSECS, PENG, …) are specified. Others are under “Case Else”. (05/10/2021)
	     . Included K1,K2 from Shockman and Byrne (2021) to match PyCO2SYS and the CO2SYS-MATLAB v3.2.0 (05/19/2021)
             . Bug fix: in calculations involving Alkalinity and pH, the FREEtoSWS factor was misspelled FREEoSWS. Corrected. (05/17/2022)
	     . Bug fix: Somehow, sometimes, input parameters were not read properly. Now includes an “InputOK” variable. If not OK, msg to check input and restart (10/05/2022)
	     . Bug fix: made UnitFac a variant(deleted “as double”). On some computer, would get “overflow” error when trying to make UnitFac = 1000000#. (10/05/2022)
	     . Bug fix: Freshwater option has (KB, KPs, etc…set to 0, which created an issue when calculating pKs. Now pK=-999 when K=0. Also, since S=0 for that option, S output in data is also set to 0, regardless of S value entered in Column A (08/29/2023)



 