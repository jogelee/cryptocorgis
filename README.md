# cryptocorgis

The notebook requests the OpenSea API for every claimed Crypto Corgi. The data pulled includes Corgi number, block number, Corgi traits, sale/auction status, listed price/minimum bid, and largest offer.

The claimed_corgis.csv file is a list of blocks associated with a claimed Corgi, as of the last time the notebook was run. With each run the csv will be udpated with any new claimed Corgi blocks.

The main function, crawlOpenSea(), will pull all Corgis that are known to be claimed according to claimed_corgis.csv. The function is then run a second time on blocks between the last claimed block and the latest Ethereum block, capturing any recently claimed Corgis.

The final dataframe is output to crypto_corgis_df.csv, and can be visualized using the PandasGUI package.
