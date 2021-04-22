# Networks

## There are two code for generating...
<ul>
  <li> Random newtork </li>
  <li> Scale-free network </li>
</ul>

## What are they?  
>The radnom network model assumes that we add links between nodes *at random*.  
>Yet, most real networks new nodes prefer to link to the more connected nodes, a process called preferential attachment.  
>
>The Barabási-Albert Model, also known as BA model or *scale-free network*, is defined as below.  
>We start with m<sub>0</sub> nodes, the links between which are chosen arbitrarily, as long as each node has at least one link.  
>> <b>Growth</b>  
>>At each time step we add a new node with *m* links (less than m<sub>0</sub>) that connect the new node to *m* nodes already in the network.  
>>  
>> <b>Preferential attachment</b>  
>>The probability that a link of the new node connects to node *i* depends on the degree *k<sub>i</sub>* as below  
>><img src="https://latex.codecogs.com/png.image?\dpi{130}&space;\bg_white&space;\prod(k_i)=\frac{k_i}{\sum_{j}^{}k_j}" title="\bg_black prod(k_i)=\frac{k_i}{\sum_{j}^{}k_j}" />
>>

>Then, how degree distribution of the scale-free network looks like?  
>Let us approximate the degree *k<sub>i</sub>* with a continuous real variable, representing its expectation value over many realizations of the growth process.  
><img src="https://latex.codecogs.com/png.image?\dpi{120}&space;\bg_white&space;\frac{dk_i}{dt}=m\prod_{}^{}(k_i)=m\frac{k_i}{\sum_{j=1}^{N-1}k_j}" title="\bg_black \frac{dk_i}{dt}=m\prod_{}^{}(k_i)=m\frac{k_i}{\sum_{j=1}^{N-1}k_j}" />  
><img src="https://latex.codecogs.com/png.image?\dpi{120}&space;\bg_white&space;\sum_{j=1}^{N-1}k_j=2mt-m" title="\bg_white \sum_{j=1}^{N-1}k_j=2mt-m" />  
><img src="https://latex.codecogs.com/png.image?\dpi{120}&space;\bg_white&space;\frac{dk_i}{dt}=\frac{k_i}{2t-1}" title="\bg_white \frac{dk_i}{dt}=\frac{k_i}{2t-1}" />  
>By integrating upper equation using the fact that *k<sub>i</sub>(t<sub>i</sub>)=m*, we obtain  
><img src="https://latex.codecogs.com/png.image?\dpi{120}&space;\bg_white&space;k_i(t)=m(\frac{t}{t_i})^{1/2}" title="\bg_white k_i(t)=m(\frac{t}{t_i})^{1/2}" />  
><img src="https://latex.codecogs.com/png.image?\dpi{120}&space;\bg_white&space;P(k_i)=\frac{\partial&space;(k_i(t)<k)}{\partial&space;k" title="\bg_white P(k_i)=\frac{\partial k_i(t)<k}{\partial k" />  
><img src="https://latex.codecogs.com/png.image?\dpi{120}&space;\bg_white&space;P(k_i(t)<k)=P(m(\frac{t}{t_i})^{\frac{1}{2}})<k" title="\bg_white P(k_i(t)<k)=P(m(\frac{t}{t_i})^{\frac{1}{2}})<k" />  
><img src="https://latex.codecogs.com/png.image?\dpi{120}&space;\bg_white&space;P(t_i>t(\frac{m}{k})^{1/\beta})=1-P(t_i\leq&space;t(\frac{m}{k})^{1/\beta})=1-(\frac{m}{k})^{1/\beta}" title="\bg_white P(t_i>t(\frac{m}{k})^{1/\beta})=1-P(t_i\leq t(\frac{m}{k})^{1/\beta})=1-(\frac{m}{k})^{1/\beta}" />  
><img src="https://latex.codecogs.com/png.image?\dpi{120}&space;\bg_white&space;P(k)=\frac{\partial&space;P(k_i(t)<k)}{\partial&space;k}=\frac{1}{\beta}\frac{m^{1/\beta}}{k^{1/\beta&plus;1}}=2m^{2}k^{-3}" title="\bg_white P(k)=\frac{\partial P(k_i(t)<k)}{\partial k}=\frac{1}{\beta}\frac{m^{1/\beta}}{k^{1/\beta+1}}=2m^{2}k^{-3}" />  
>  
>Now you can see the degree distribution has *power-law* tail!
>>[Network Science by Albert-László Barabási] (http://networksciencebook.com/chapter/5#growth)  
