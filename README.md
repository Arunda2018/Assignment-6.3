# Assignment-6.3
library(MASS)
> step_fit <- stepAIC(fit,method='backward')
Start:  AIC=2210.8
churn ~ state + account_length + area_code + international_plan + 
    voice_mail_plan + number_vmail_messages + total_day_minutes + 
    total_day_calls + total_day_charge + total_eve_minutes + 
    total_eve_calls + total_eve_charge + total_night_minutes + 
    total_night_calls + total_night_charge + total_intl_minutes + 
    total_intl_calls + total_intl_charge + number_customer_service_calls

                                Df Deviance    AIC
- state                         50   2158.3 2198.3
- area_code                      2   2071.2 2207.2
- total_night_calls              1   2070.8 2208.8
- total_day_minutes              1   2070.8 2208.8
- total_day_charge               1   2070.8 2208.8
- total_night_minutes            1   2070.9 2208.9
- total_night_charge             1   2070.9 2208.9
- total_eve_calls                1   2070.9 2208.9
- total_eve_charge               1   2071.1 2209.1
- total_eve_minutes              1   2071.1 2209.1
- account_length                 1   2071.3 2209.3
- total_intl_minutes             1   2071.4 2209.4
- total_intl_charge              1   2071.4 2209.4
<none>                               2070.8 2210.8
- total_day_calls                1   2072.8 2210.8
- number_vmail_messages          1   2075.1 2213.1
- total_intl_calls               1   2083.9 2221.9
- voice_mail_plan                1   2084.9 2222.9
- number_customer_service_calls  1   2250.7 2388.7
- international_plan             1   2272.4 2410.4

Step:  AIC=2198.28
churn ~ account_length + area_code + international_plan + voice_mail_plan + 
    number_vmail_messages + total_day_minutes + total_day_calls + 
    total_day_charge + total_eve_minutes + total_eve_calls + 
    total_eve_charge + total_night_minutes + total_night_calls + 
    total_night_charge + total_intl_minutes + total_intl_calls + 
    total_intl_charge + number_customer_service_calls

                                Df Deviance    AIC
- area_code                      2   2158.7 2194.7
- total_day_minutes              1   2158.3 2196.3
- total_day_charge               1   2158.3 2196.3
- total_night_minutes            1   2158.3 2196.3
- total_night_charge             1   2158.3 2196.3
- total_night_calls              1   2158.3 2196.3
- total_eve_calls                1   2158.4 2196.4
- total_eve_charge               1   2158.5 2196.5
- total_eve_minutes              1   2158.5 2196.5
- account_length                 1   2158.6 2196.6
- total_intl_minutes             1   2158.9 2196.9
- total_intl_charge              1   2158.9 2196.9
- total_day_calls                1   2159.6 2197.6
<none>                               2158.3 2198.3
- number_vmail_messages          1   2162.3 2200.3
- voice_mail_plan                1   2171.8 2209.8
- total_intl_calls               1   2172.7 2210.7
- number_customer_service_calls  1   2335.5 2373.5
- international_plan             1   2347.8 2385.8

Step:  AIC=2194.72
churn ~ account_length + international_plan + voice_mail_plan + 
    number_vmail_messages + total_day_minutes + total_day_calls + 
    total_day_charge + total_eve_minutes + total_eve_calls + 
    total_eve_charge + total_night_minutes + total_night_calls + 
    total_night_charge + total_intl_minutes + total_intl_calls + 
    total_intl_charge + number_customer_service_calls

                                Df Deviance    AIC
- total_day_minutes              1   2158.7 2192.7
- total_day_charge               1   2158.7 2192.7
- total_night_minutes            1   2158.7 2192.7
- total_night_charge             1   2158.8 2192.8
- total_night_calls              1   2158.8 2192.8
- total_eve_calls                1   2158.9 2192.9
- total_eve_charge               1   2159.0 2193.0
- total_eve_minutes              1   2159.0 2193.0
- account_length                 1   2159.1 2193.1
- total_intl_minutes             1   2159.4 2193.4
- total_intl_charge              1   2159.4 2193.4
- total_day_calls                1   2160.1 2194.1
<none>                               2158.7 2194.7
- number_vmail_messages          1   2162.7 2196.7
- voice_mail_plan                1   2172.3 2206.3
- total_intl_calls               1   2173.3 2207.3
- number_customer_service_calls  1   2335.7 2369.7
- international_plan             1   2348.3 2382.3

Step:  AIC=2192.73
churn ~ account_length + international_plan + voice_mail_plan + 
    number_vmail_messages + total_day_calls + total_day_charge + 
    total_eve_minutes + total_eve_calls + total_eve_charge + 
    total_night_minutes + total_night_calls + total_night_charge + 
    total_intl_minutes + total_intl_calls + total_intl_charge + 
    number_customer_service_calls

                                Df Deviance    AIC
- total_night_minutes            1   2158.8 2190.8
- total_night_charge             1   2158.8 2190.8
- total_night_calls              1   2158.8 2190.8
- total_eve_calls                1   2158.9 2190.9
- total_eve_charge               1   2159.0 2191.0
- total_eve_minutes              1   2159.0 2191.0
- account_length                 1   2159.1 2191.1
- total_intl_minutes             1   2159.4 2191.4
- total_intl_charge              1   2159.4 2191.4
- total_day_calls                1   2160.1 2192.1
<none>                               2158.7 2192.7
- number_vmail_messages          1   2162.7 2194.7
- voice_mail_plan                1   2172.3 2204.3
- total_intl_calls               1   2173.3 2205.3
- total_day_charge               1   2316.9 2348.9
- number_customer_service_calls  1   2335.7 2367.7
- international_plan             1   2348.3 2380.3

Step:  AIC=2190.75
churn ~ account_length + international_plan + voice_mail_plan + 
    number_vmail_messages + total_day_calls + total_day_charge + 
    total_eve_minutes + total_eve_calls + total_eve_charge + 
    total_night_calls + total_night_charge + total_intl_minutes + 
    total_intl_calls + total_intl_charge + number_customer_service_calls

                                Df Deviance    AIC
- total_night_calls              1   2158.8 2188.8
- total_eve_calls                1   2158.9 2188.9
- total_eve_charge               1   2159.0 2189.0
- total_eve_minutes              1   2159.0 2189.0
- account_length                 1   2159.1 2189.1
- total_intl_minutes             1   2159.4 2189.4
- total_intl_charge              1   2159.4 2189.4
- total_day_calls                1   2160.1 2190.1
<none>                               2158.8 2190.8
- number_vmail_messages          1   2162.8 2192.8
- total_night_charge             1   2169.9 2199.9
- voice_mail_plan                1   2172.3 2202.3
- total_intl_calls               1   2173.4 2203.4
- total_day_charge               1   2316.9 2346.9
- number_customer_service_calls  1   2335.9 2365.9
- international_plan             1   2348.3 2378.3

Step:  AIC=2188.81
churn ~ account_length + international_plan + voice_mail_plan + 
    number_vmail_messages + total_day_calls + total_day_charge + 
    total_eve_minutes + total_eve_calls + total_eve_charge + 
    total_night_charge + total_intl_minutes + total_intl_calls + 
    total_intl_charge + number_customer_service_calls

                                Df Deviance    AIC
- total_eve_calls                1   2159.0 2187.0
- total_eve_charge               1   2159.1 2187.1
- total_eve_minutes              1   2159.1 2187.1
- account_length                 1   2159.2 2187.2
- total_intl_minutes             1   2159.5 2187.5
- total_intl_charge              1   2159.5 2187.5
- total_day_calls                1   2160.1 2188.1
<none>                               2158.8 2188.8
- number_vmail_messages          1   2162.8 2190.8
- total_night_charge             1   2170.0 2198.0
- voice_mail_plan                1   2172.3 2200.3
- total_intl_calls               1   2173.4 2201.4
- total_day_charge               1   2317.3 2345.3
- number_customer_service_calls  1   2335.9 2363.9
- international_plan             1   2348.6 2376.6

Step:  AIC=2186.96
churn ~ account_length + international_plan + voice_mail_plan + 
    number_vmail_messages + total_day_calls + total_day_charge + 
    total_eve_minutes + total_eve_charge + total_night_charge + 
    total_intl_minutes + total_intl_calls + total_intl_charge + 
    number_customer_service_calls

                                Df Deviance    AIC
- total_eve_charge               1   2159.2 2185.2
- total_eve_minutes              1   2159.2 2185.2
- account_length                 1   2159.3 2185.3
- total_intl_minutes             1   2159.6 2185.6
- total_intl_charge              1   2159.7 2185.7
- total_day_calls                1   2160.3 2186.3
<none>                               2159.0 2187.0
- number_vmail_messages          1   2162.9 2188.9
- total_night_charge             1   2170.1 2196.1
- voice_mail_plan                1   2172.4 2198.4
- total_intl_calls               1   2173.5 2199.5
- total_day_charge               1   2317.7 2343.7
- number_customer_service_calls  1   2336.0 2362.0
- international_plan             1   2348.7 2374.7

Step:  AIC=2185.2
churn ~ account_length + international_plan + voice_mail_plan + 
    number_vmail_messages + total_day_calls + total_day_charge + 
    total_eve_minutes + total_night_charge + total_intl_minutes + 
    total_intl_calls + total_intl_charge + number_customer_service_calls

                                Df Deviance    AIC
- account_length                 1   2159.6 2183.6
- total_intl_minutes             1   2159.9 2183.9
- total_intl_charge              1   2159.9 2183.9
- total_day_calls                1   2160.5 2184.5
<none>                               2159.2 2185.2
- number_vmail_messages          1   2163.1 2187.1
- total_night_charge             1   2170.4 2194.4
- voice_mail_plan                1   2172.6 2196.6
- total_intl_calls               1   2173.7 2197.7
- total_eve_minutes              1   2200.5 2224.5
- total_day_charge               1   2318.3 2342.3
- number_customer_service_calls  1   2336.4 2360.4
- international_plan             1   2348.8 2372.8

Step:  AIC=2183.56
churn ~ international_plan + voice_mail_plan + number_vmail_messages + 
    total_day_calls + total_day_charge + total_eve_minutes + 
    total_night_charge + total_intl_minutes + total_intl_calls + 
    total_intl_charge + number_customer_service_calls

                                Df Deviance    AIC
- total_intl_minutes             1   2160.2 2182.2
- total_intl_charge              1   2160.3 2182.3
- total_day_calls                1   2160.9 2182.9
<none>                               2159.6 2183.6
- number_vmail_messages          1   2163.5 2185.5
- total_night_charge             1   2170.7 2192.7
- voice_mail_plan                1   2172.9 2194.9
- total_intl_calls               1   2174.0 2196.0
- total_eve_minutes              1   2200.7 2222.7
- total_day_charge               1   2318.8 2340.8
- number_customer_service_calls  1   2337.1 2359.1
- international_plan             1   2349.9 2371.9

Step:  AIC=2182.24
churn ~ international_plan + voice_mail_plan + number_vmail_messages + 
    total_day_calls + total_day_charge + total_eve_minutes + 
    total_night_charge + total_intl_calls + total_intl_charge + 
    number_customer_service_calls

                                Df Deviance    AIC
- total_day_calls                1   2161.6 2181.6
<none>                               2160.2 2182.2
- number_vmail_messages          1   2164.1 2184.1
- total_night_charge             1   2171.4 2191.4
- voice_mail_plan                1   2173.5 2193.5
- total_intl_calls               1   2174.5 2194.5
- total_intl_charge              1   2179.2 2199.2
- total_eve_minutes              1   2201.3 2221.3
- total_day_charge               1   2319.8 2339.8
- number_customer_service_calls  1   2337.7 2357.7
- international_plan             1   2350.0 2370.0

Step:  AIC=2181.62
churn ~ international_plan + voice_mail_plan + number_vmail_messages + 
    total_day_charge + total_eve_minutes + total_night_charge + 
    total_intl_calls + total_intl_charge + number_customer_service_calls

                                Df Deviance    AIC
<none>                               2161.6 2181.6
- number_vmail_messages          1   2165.5 2183.5
- total_night_charge             1   2172.9 2190.9
- voice_mail_plan                1   2175.0 2193.0
- total_intl_calls               1   2176.1 2194.1
- total_intl_charge              1   2180.7 2198.7
- total_eve_minutes              1   2202.3 2220.3
- total_day_charge               1   2321.6 2339.6
- number_customer_service_calls  1   2338.5 2356.5
- international_plan             1   2351.2 2369.2
> summary(step_fit)

Call:
glm(formula = churn ~ international_plan + voice_mail_plan + 
    number_vmail_messages + total_day_charge + total_eve_minutes + 
    total_night_charge + total_intl_calls + total_intl_charge + 
    number_customer_service_calls, family = binomial(link = "logit"), 
    data = churnTrain)

Deviance Residuals: 
    Min       1Q   Median       3Q      Max  
-3.2421   0.1969   0.3375   0.5133   2.1204  

Coefficients:
                               Estimate Std. Error z value Pr(>|z|)    
(Intercept)                    8.067161   0.515870  15.638  < 2e-16 ***
international_planyes         -2.040338   0.145243 -14.048  < 2e-16 ***
voice_mail_planyes             2.003234   0.572352   3.500 0.000465 ***
number_vmail_messages         -0.035262   0.017964  -1.963 0.049654 *  
total_day_charge              -0.076589   0.006371 -12.022  < 2e-16 ***
total_eve_minutes             -0.007182   0.001142  -6.290 3.17e-10 ***
total_night_charge            -0.082547   0.024653  -3.348 0.000813 ***
total_intl_calls               0.092176   0.024988   3.689 0.000225 ***
total_intl_charge             -0.326138   0.075453  -4.322 1.54e-05 ***
number_customer_service_calls -0.512256   0.039141 -13.087  < 2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

(Dispersion parameter for binomial family taken to be 1)

    Null deviance: 2758.3  on 3332  degrees of freedom
Residual deviance: 2161.6  on 3323  degrees of freedom
AIC: 2181.6

Number of Fisher Scoring iterations: 6

> confint(step_fit)
Waiting for profiling to be done...
                                     2.5 %        97.5 %
(Intercept)                    7.070889530  9.0938386274
international_planyes         -2.326003857 -1.7562369114
voice_mail_planyes             0.907323062  3.1529598406
number_vmail_messages         -0.070725900 -0.0002376739
total_day_charge              -0.089209954 -0.0642271566
total_eve_minutes             -0.009433875 -0.0049559927
total_night_charge            -0.131007646 -0.0343300642
total_intl_calls               0.043965614  0.1419403277
total_intl_charge             -0.474987860 -0.1790890316
number_customer_service_calls -0.589558964 -0.4360233938
> #ANOVA on base model
> anova(fit,test = 'Chisq')
Analysis of Deviance Table

Model: binomial, link: logit

Response: churn

Terms added sequentially (first to last)


                              Df Deviance Resid. Df Resid. Dev  Pr(>Chi)    
NULL                                           3332     2758.3              
state                         50   83.184      3282     2675.1 0.0022252 ** 
account_length                 1    1.221      3281     2673.9 0.2691078    
area_code                      2    0.081      3279     2673.8 0.9602791    
international_plan             1  175.984      3278     2497.8 < 2.2e-16 ***
voice_mail_plan                1   43.206      3277     2454.6 4.928e-11 ***
number_vmail_messages          1    3.785      3276     2450.8 0.0517159 .  
total_day_minutes              1  130.345      3275     2320.5 < 2.2e-16 ***
total_day_calls                1    1.314      3274     2319.2 0.2516785    
total_day_charge               1    0.020      3273     2319.2 0.8879159    
total_eve_minutes              1   31.752      3272     2287.4 1.752e-08 ***
total_eve_calls                1    0.177      3271     2287.2 0.6738425    
total_eve_charge               1    0.610      3270     2286.6 0.4348650    
total_night_minutes            1    8.859      3269     2277.8 0.0029160 ** 
total_night_calls              1    0.023      3268     2277.7 0.8793045    
total_night_charge             1    0.385      3267     2277.3 0.5348351    
total_intl_minutes             1   12.482      3266     2264.9 0.0004108 ***
total_intl_calls               1   13.740      3265     2251.1 0.0002099 ***
total_intl_charge              1    0.472      3264     2250.7 0.4919867    
number_customer_service_calls  1  179.849      3263     2070.8 < 2.2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
> #ANOVA from reduced model after applying the Step AIC
> anova(step_fit,test = 'Chisq')
Analysis of Deviance Table

Model: binomial, link: logit

Response: churn

Terms added sequentially (first to last)


                              Df Deviance Resid. Df Resid. Dev  Pr(>Chi)    
NULL                                           3332     2758.3              
international_plan             1  170.400      3331     2587.9 < 2.2e-16 ***
voice_mail_plan                1   41.868      3330     2546.0 9.765e-11 ***
number_vmail_messages          1    3.638      3329     2542.4 0.0564756 .  
total_day_charge               1  135.452      3328     2406.9 < 2.2e-16 ***
total_eve_minutes              1   30.874      3327     2376.1 2.753e-08 ***
total_night_charge             1    8.500      3326     2367.6 0.0035509 ** 
total_intl_calls               1   12.887      3325     2354.7 0.0003309 ***
total_intl_charge              1   16.210      3324     2338.5 5.668e-05 ***
number_customer_service_calls  1  176.839      3323     2161.6 < 2.2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
> #plot the fitted model
> plot(fit$fitted.values)
