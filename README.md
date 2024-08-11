# Price Prediction of Local Agriculture Products
Accurate price forecasting is essential to ensure the stable and efficient supply of local specialty products such as cabbage, radish, tangerines, and more.

## Description
I have been developing an effective AI model with the goal of augmenting of accuracy for price prediction and uncovering valuable insights related to these products, using CatBoost, XGBoost etc.

### Dataset Information
**1. train.csv**
- train data: Price data of distributed items from 01/01/2019 to 03/03/2023
- item code: TG=Tangerine, BC=Broccoli, RD=Radish, CR=Carrot, CB=Cabbage
- corporation: Distribution corporation code, ranging from corporation A to F location
- Location code: J=Jeju, S=Seogwipo
- supply(kg): Distributed quantity in kilograms
- price(won/kg): Price per kilogram of the distributed items in Korean Won

**2. international_trade.csv**
- international trade information: Import and export information for related items

**3. test.csv**
- test data: Data from 03/04/2023 to 03/31/2023

**4. sample_submission.csv**
- submission format: Predict price(won/kg) from 03/04/2023 to 03/31/2023
- ID: Identifier consisting of item, corporation and location codes
- must fill in the predicted price(won/kg) in the answer column for the corresponding ID

### Approaches
- Preprocessing: Remove extreme outliers
- Modeling and training prediction: Define ensemble models and voting

## Outline
0. Load Data
1. Preprocessing
2. Products excluding TG(Tangerine)
3. TG(1) (Tangerine)
4. TG(2) (Generalization)
5. TG Ensemble
6. Post-processing
