# Empirical-Statistical-Bias-Correction-and-Downscaling
Downscaling is essential for assessing climate change impacts at regional or local scales because global climate models (GCMs) typically operate at coarse spatial resolutions (100–300 km), which are inadequate for capturing local climate variations. While GCMs provide insights into global climate trends, their outputs are not directly applicable for local-scale impact assessments due to large biases and uncertainties, particularly when it comes to extreme events \citep{gebrechorkos2023high, navarro2020high}. This limitation poses challenges for decision-making processes in critical sectors like energy, water resources, and agriculture, where detailed, location-specific climate data is needed to plan for climate change impacts effectively. 

Empirical-statistical downscaling \citep{kotamarthi2021downscaling, benestad2008empirical} addresses this challenge by adjusting GCM outputs to finer spatial and temporal scales. It establishes a statistical relationship between observed data (e.g., from weather stations, satellites, or reanalyses) and GCM projections, which is then used to downscale future climate scenarios to a resolution relevant for local impact assessments. By efficiently refining coarse climate projections, statistical downscaling provides high-resolution data tailored to regional conditions, making it a practical tool for climate change studies across diverse sectors and regions \citep{gebrechorkos2023high}. 

In the present analysis we use empirical-statistical bias correction and downscaling to adjust CMIP6 projections to fit the observed distributions. The methodology follows three major steps: bias correction using quantile mapping, downscaling from daily to hourly scales, and validation of downscaled data.

subsubsection{Bias Correction using Quantile Mapping}

The quantile mapping approach (section 3.2.5 \citet{teutschbein2012bias}) aligns the cumulative distribution functions (CDFs) of CMIP6 model data and ERA5 or any other observations data over a historical period, then applies this relationship to the future projections. The process steps are as follows for all variables except precipitation:

item Fit normal distributions to observed and simulated data:
    
$`\begin{equation}  X \sim \mathcal{N}(\mu, \sigma).\end{equation} \end{equation} `$
    
##### New addition 
