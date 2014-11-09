---
layout: page
title: "AIRS Memo: Array M8 A/B-side Variations With Time"
date: 2012-12-10 18:05
comments: true
sharing: true
footer: true
---
* Dummy header for TOC
{:toc}

# Summary

There are observable radiometric differences between the AIRS module
M8 A- and B-side detectors.  We have been working to determine how
these differences vary with scene temperature.  However, we first
looked at the time dependence of these differences and found that they
are changing with time.  This was observed by L. Strow about 1 year
ago looking at the time rate of change of AIRS/IASI SNOs.  

# Data
The following set of M8 channels are used in this study.  None of
these channels are on the bad channel list (current as of Margie
Weiler's last email on 12/1/2012).  In addition, none of these
channels had their A/B states changes after Nov. 2003.  (Some did
before Nov. 2003, so these results are only partially valid previous
to Nov. 2003.) Channels used were:

| A-side              |  |B-Side  |
| 623 639 651 659 669 |  |642 644 |
| 690 703 706 716 731 |  |656 658 |
| 734 739 744 750 751 |  |684 698 |
| 754 762 764 766 769 |  | 727    |

Figure 1: Top (B-side) and Bottom (A-side) M8 detector bias for clear
scenes.  Time scale is 10 years.  

{% include aslfig.html width="440" url="/images/strow/Aside_Bside_gridded_vs_time.png" description="Fig. 1 caption here" %}

The channel biases were observed minus computed ocean scenes using the
ERA-interim reanalysis.  The raw data are daily averages of these
data, and include all latitudes with clear ocean scenes.  

Figure 1 shows a gridded plot of the time development of
these channels over 10 years.  The gridding was done to determine if
any of the channels exhibits poor noise behavior, at least averaged
over 20 day spans shown in this figure.  Examination of this plot
indicates that there is no significant change in noise in these
groups of channels.  Note that *all* channel biases for daily
averages are shown here, although some gross scene selection is done
when we produce these clear subset files, generally we required the
bias for the 1231 wavenumber channel to be in the range of $\pm$ 25K.

Figure 2: Variation in A-side minus B-side radiances versus 1231 wavenumber
B(T).

{% include aslfig.html width="440" url="/images/strow/ab_vs_bt1231_withdcc.png" description="Fig. 2 a caption"  %}

We have also examined the ACDS DCC data, and computed the difference
in the Observed B(T) differences (not the bias) for these data, for
the M8 A-,B-side detectors.  Figure 2 shows how these A- and B-side
differences change with the overall observing scene temperature (using
1231 wavenumber B(T) as a proxy).  Note we used several different data
sets for this figure; (a) for the clear data subset all times after
Dec. 2003, and all times after Sept. 2009, and (b) for the DCC data
all times after Nov. 2003 and but before Sept. 2009, and just time
after Sept. 2009.  Note that the time period selection has a large
effect for the DCC data.

Figure 3: Time series of A- and B-side bias differences (for clear)
and A- and B-side BT(obs) for DCC's.  Note the DCC data has been
divided by 5.

{% include aslfig.html url="/images/strow/ab_bias_vs_time_eachday_with_dcc.png" width="440" description="Fig. 3 caption" %}

The reason for time subsetting the previous results is shown in
Fig. 3.  Blue is the daily difference between the
average bias of the 20 A-side minus the average bias of the 7 B-side
M8 detectors.  No time averaging other than daily has been performed
here.  Red is the standard deviation over the 140 combinations of A
minus B detectors.  Also shown in the daily difference of the observed
B(T)'s between the A- and B-side DCC spectra.  Clearly, around
Sept. 2009 something happened to change the A-side detector radiances.
If one looks carefully at the blue curve, very small offsets are noted
due to the Jan. 2010 shutdown of AIRS.

These observations complicate any attempt to reconcile differences
between the M8 A- and B-side detectors, and probably should be
studied more before any work to parameterize these differences as a
function of scene temperature.  

Our next step will be to try to fill in the missing scene
temperatures in Fig. 2 using BT(obs) data for a very
large statistical set.  This data set will have to be subsetted in
time similarly to what is shown already.  

