# Statistical Distances Exploration

## Statistical Distance Overview

- Statistical distance is simply a measure of distance between two probability distributions or random variables, where what qualifies as the distance is defined by the chosen distance measure.
    - There are statistical distances that satisfy the requirements for a metric, but not all statistical distances are metrics. (Metrics in the rigorous mathematical sense)


## Distance Measures

### Kullback-Leibler Distance (KLD)
- Discrete: D_KL(P|Q) = sum_i( P(i) * log( P(i) / Q(i) ) )
- Continuous: D_KL(P|Q) = int_-inf^inf p(x) * 
    - P(i) and Q(i) are proabilities

### Symmetric KLD

### Hellinger Distance 

### Renyi Divergence

### Jensen-Shannon Divergence

### Bhattacharyya Distance

### Wasserstein Metric

### Bregman Divergence



## Test Matrix

- what needs to be tested under what conditions?
- 9 distances : 9 -> cut to 5, some intermediate testing to find really shitty ones
- starting number of gaussians: 100-1000 by 100 : 100 -> 100,400,700,1000
- middle number of clusters and cluster final size (number of mixands per cluster after condensation): 2-5% by 1's of starting number of mixands : 4
- end number of gaussians: 10-50% by 10's of starting mixands : 5 -> 10,30,50
- dimensions: 1,2,4 : 3
- 10 starting mixutres -> 10 -> 5
- runnells base case for every distance, starting, mid, repeat, dimension

- **total: 7200 tests** -> **12960** -> **7200**

based on dimesion and starting number, generate random mixture, use for all mid nums, end nums, distances

- repeatabiltiy
- dimensions
    - starting number
        - generate mixture
            - all mid nums
                - end nums
                    - distance
                        - run kmeans
                        - SAVE ME!
                    - runnells
                        - SAVE ME! AGAIN!

- saving: one big file!
    - excecution time
    - ISD
    - starting mixtures
    - paremeters -> matrix with all params, with tuples of ISD and excecution time

- look into hdf5 for managing data

- cut kld in favor of symmetric kld
                        