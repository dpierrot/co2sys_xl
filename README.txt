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

 