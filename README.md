# dacon3
#Predicting Final Bid of the Apartment

DATA DESCRIPTION
-----------------

Background

 

There are three main ways to buy a house in Korea.

The 1st way is to choose appropriate apartment through the real estate agents or

the 2nd is to buy an apartment from the constructor.

The 3rd way is to use the real estate auctions.

 

In general, Korean feel difficult it and they think that they cannot even begin to get started.

They are worried that if they make a reckless move without knowing the laws related to the analysis of rights and related to the laws,

they could lose their seed money.

 

Is the real estate auction really difficult and dangerous?

 

Yoon Soohyun(39 old) author of “the 365-month rent account”,

She said in an interview in the Hankook Daily(Korea newspaper) “It is just a misunderstanding and prejudice.”

 

The author argues that the more seed money is lacking, the more we should find a way at auction. 

- An excerpt from the Hankook Ilbo(Korea Newspaper).

 Challenge auction with seed money of 10 million won( 1130.56 won per 1$)... The Monthly Rent rich woman in only Three Years.

http://www.hankookilbo.com/News/Read/201804170416692333

 

Recently, various real estate related financial products such as real estate funds are actively being developed based on diverse data,

and expertise such as the development of high-yield investment products, trust in real estate investment,

evaluation of profitability and management of data is required.

 

The data for this contest was provided by a company that specializes in information services related to real estate auctions.
Infocare Auction(http://www.infocare.co.kr)

 

We hope many people will be interested in the data on apartment auction,

participate in the competition and realize your dream of own house.

 

Description

 

Existing financial institutions have conducted a review based on FICO scores and collateral oriented. On the other side,

The Korean FinTech company, TOGETHER FUNDING, 

predicts winning bid price and aims to provide financial opportunities for top winning bidders with low credit scores or with little collateral.

 

Please make a model to predict the apartment hammer price at this competition.

Together, we determine whether to lend or not based on the hammer price.

The more accurate the model is, the less the loss.

 

Order of auction procedure

flow

 

https://pds.joins.com/news/component/brandnews/201106/08/kumsol_813655_OEC3Kx.jpg

 

Validation

 

You are provided about 2,700 auction apartments information for 2 years in Seoul and Busan, Korea. with various data tables,

including registration, rent, appraised price, number of miscarriage, location information, hammer price, etc.

The main mission(goal) is to predict the hammer price of given apartments.

 

* You can use external data(public data) that is not subject to legal restrictions such as ‘The Apartment Real Transaction Price of the Ministry of Land,

Infrastructure, and Transport’ (http://rt.molit.go.kr).

 

Submissions are evaluated with a cost function, using the following Root Mean Squared Error(RMSE). (Evaluations are based on provided datasets only.)

 Players with the lowest score will be nominated for awards, tie players are ranked high most recent submission. Ranking can change after code validation.

Candidates have to submit code file(s) with annotation(English or Korean) or documentation fills in with an explanation.

 

code validation contents(model validation)

1. Pre-Processing for Data Cleaning

2. Feature Engineering and Variable Selection

3. Model Selection and Regularization

4. Optimization Processing

 

[Files]

 

1. Auction_master_train_en.csv – Basic information such as the location, appraiser, and the start/end date of the auction including the hammer price of the Seoul/Busan area (*last 2 years).

2. Auction_master_test_en.csv – Same with train.csv except for hammer price data. 

3. Auction_submission_en.csv – Fill in with predicting hammer price.

4. Auctiuon_regist_en.csv – a certified copy of the register on apartments.

 

*The registration information may be missing if any of the following occurs during an individual auction.


    a. If all registration of items are the same (only one is issued). 

b. If it is difficult to issue a copy of the registration due to excessive registration (for example, if you cannot issue a certified copy of the registration due to too many registered creditors, owners, etc.).

 

*Individual auction: Case of auction is held with multiple items for one event number.

 

*Excessive registration : Case of the number of registered persons exceeds 100. 

 

5. Auctiuon_result_en.csv – Auction date, appraised price, minimum sales price, auction result, etc.

6. Auctiuon_rent_en.csv – Data such as rent, transfer/ownership, deposit, and monthly rent, etc.

 

Term auction (Refer to below URL.)

(https://www.courtauction.go.kr/RetrieveAucTermInq.laf)

 

[Data fields]

 

Auction_master_test_en.csv & Auction_master_train_en.csv 

Auction_key

Unique key values for the auction house.

Auction_class

Auction classification

 

forced auction: Carrying out the auction according to the executive authority after litigation and judgment.

 

random auctions: Carrying out the auction with a copy of the registration book (collateral, provisional attachment, etc.).

 

(http://www.xn--289al3wfvfg7fo3dqso.com/?c=35/164/169/168&where=subject%7Ctag&keyword=%EC%9E%84%EC%9D%98&uid=913
http://www.goodmorningcc.com/news/articleView.html?idxno=50150)

Bid_class

Bid classification. individual, bundle, general.

Claim_price

the amount of the applicant's claim.

Appraisal_company

Appraiser.

Appraisal_date

Appraisal date.

Auction_count

A total number of appraisal.

Auction_miscarriage_count

A total number of miscarriages.

Total_land_gross_area

Total land gross area(㎡).

Total_land_real_area

Total land real area(㎡).

Total_land_auction_area

Total land auction area(㎡).

Total_building_area

Total building area(㎡).

Total_building_auction_area

Total building auction area(㎡).

Total_appraisal_price

Total appraisal price.

Minimum_sales_price

Minimum sales price, the minimum amount that the bidder has to offer in the bid.

First_auction_date

First auction date.

Final_auction_date

Final auction date.

Final_result

A final result of an auction.

Creditor

The creditors, an auctioneer.

addr_etc

Other address

Apartment_usage

Usage of the apartment.

Completion_date

Completion date.

Preserve_regist_date

Preserve registration date, new building and registration for the first time.

Total_floor

Total floors.

Current_floor

Current floor.

Share_auction_YorN

Stake auction status (Y/N), Only a part of a real estate is not a whole but auction is proceeded (a shareholder of one real estate owns ownership as a stake, and a part of them is auctioned).

Close_date

Auction close date

Close_result

Close result, the difference between winning and paying dividends :

:
Auction procedure① Auction procedure (a winning bid

) ▷ ② a winning decision ▷ ③ Payment ▷ ④ end after dividend

 

With the winning bid price, the court gives the creditor priority and the auction closes.

point.y

Latitude.

point.x

Longitude.

addr_en

Converted Korean address to English address

Hammer_price

Hammer price.

 

Auction_result_en.csv

Auction_key

Unique key values for the auction house.

Auction_seq

Sequence key of the auction result.

Auction_date

Auction date.

Appraisal_price

Appraisal price.

Minimum_sales_price

Minimum sales price, the minimum amount that the bidder has to offer in the bid.

Auction_results

Auction results

 

change : Procedure for the court to change the auction schedule with the authority when the auction cannot be held on the specified auction day for special reasons.

 

failure of an auction : Not auctioned on auction date.

 

Winning bid : the highest bid.

 

payout : Payment will be paid once the bid is approved.

 

dividend : Allotment of money in accordance with creditors' priority on paid payments.

 

Auction_regist_en.csv

Auction_key

Unique key values for the auction house.

Auction_seq

Sequence key of registration.

Regstration_type

Sort of registration (land, building, Multi owned Building)

 

Building register  : Building registration of general property.

 

land registration : Land registration of general real estate

Multi owned Building registration : Multi owned Building registration such as the apartment.

 

land separately registration : A house should be traded in combination with a piece of land. But If the land has a mortgage before it is built, the legal relationship between the land and the building may be inconsistent. Registration to mark "there is a separate registration of land" on the building register.

Regstration_class

Classification of registration

 

provisional registration : A preliminary register for the preservation of the priority of the primary register.

 

preservative measure : A provisional disposition by the court before the case is decided to preserve the right conflicting.

 

provisional attachment, injunction : Execution by the legal process of money is called provisional attachment as a result of the preservative measure. Execution by the legal process of action is called an injunction as a result of the preservative measure.

 

ownership transfer, transfer : Transfer of ownership due to contract, etc.

 

real distress : Forcing a government agency to prohibit a debtor from disposing of property or exercising rights.

 

notice registration : In the event of a lawsuit for cancellation or recovery due to invalidation or cancellation of the registration cause, registration to warn third parties.

 

compulsion, random auction : Registration made upon application of compulsory auction, random auction.

 

the right of lease : lease registration by lease registration order.

mortgage : Generally, when the creditor lends money to the property as a security, it registers on the real-estate registration.

 

right to lease on a deposit basis : registration made by the leaseholder.

 

the right of the pledge : The collateral held by the creditor as the collateral of the bond

Regist_date

Regist date, Categorized as 9999999999 for land separately registration

Creditor

A creditor listed in the certified copy of the registration

Regist_price

Registered borrowing, a loan secured against a registered real estate

 

Auction_rent_en.csv

Auction_key

Unique key values for the auction house

Rent_class

Rent classification,

move in : Date of notifying the new address (at dong office).

 

occupation : In case of a rental period or have a room occupant.

Purpose_use

Usage of the leaseholder.

Occupied_part

Occupied part of the occupant.

Rent_date

Date of the lease, date of notifying new address, if the uncertainty 11111111.

Rent_deposit

Deposit for rent.

Rent_monthly_price

Monthly rent price.

