# Dex-Screener
Pre reqs - Numpy, Prettytable, Pandas.

# Summary
- Analyzing liquidity data in a DataFrame (df).
Converts the 'liquidity_usd' column to numeric values and calculates:
Mean, median, standard deviation, minimum, and maximum liquidity.
Probability of liquidity being greater than certain thresholds (e.g., 10,000, 50,000, 100,000).
Returns a dictionary containing these statistics and probabilities.
analyze_ticks(df):

- Examining changes in liquidity between data points.
Calculating the number of upticks (increases), downticks (decreases), and no change events in liquidity.
Returns probabilities for each event (uptick, downtick, no change).
display_data(df, title):

- Displays our DataFrame in a table format using PrettyTable.
Prints the table with a specified title.
display_analysis_results(analysis_results, title):

- Displays the analysis results (mean, median, standard deviation, etc.) for liquidity using PrettyTable.
Also displays liquidity probabilities for different thresholds.
display_token_analysis(token_df, token_address):

- Analyzes and displays liquidity and tick change statistics for a specific token.
Uses the analyze_liquidity and analyze_ticks functions to calculate statistics.
Displays the results using tables if liquidity data is available.
    
Tick Probabilities for Pair Data:
+--------------------------+--------------------+
|          Event           |    Probability     |
+--------------------------+--------------------+
|  Probability of Uptick   | 0.4482758620689655 |
| Probability of Downtick  | 0.5517241379310345 |
| Probability of No Change |        0.0         |
+--------------------------+--------------------+

 chainId    dexId                                   pairAddress baseToken  \
0  solana  raydium  8pnmpHUWgb1hPeFyM8DHgyRsaiWGp9qJ98eTzgTbhD8T      TOWD   
1  solana  raydium  66cxXqzCpFttLCdMBXYykjfCEVQKag8Cv1oB5KEacd5b     PUFFY   
2  solana  raydium  94hHeSqHg9t6r5A2MZ78jSHrZUUCjbCRVWDcDTfgW8Sx    WOOFIE   
3  solana  raydium  EQtFoBFcqj6M5KWLbetkYmp9EBi33WJ6UVeLHyx4kZoW      FWON   
4  solana  raydium  9RkrCXBAEtesWuymuGzTD7aheRuYiuQtdPVHCmEqCHuo     lumio   
------
  quoteToken   priceNative    priceUsd  liquidity_usd      fdv  marketCap  
0        SOL  0.0000007098  0.00009647       35940.26    96480      96480  
1        SOL   0.000001554   0.0002112      820375.59  9389338    9389338  
2        SOL    0.00001136    0.001544      145043.66  1195971    1195971  
3        SOL  0.0000001998  0.00002714       18461.99    22663      22663  
4        SOL   0.000002456   0.0003340       70384.49   334037     334037  
------

