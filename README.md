# HDB Resale Price Predictor
## **Project Overview**
This project aims to revolutionize the Singapore property market by providing a data-driven solution to predict HDB resale prices. By leveraging machine learning models, our tool empowers property agents with accurate pricing strategies, enabling them to better serve their clients in a competitive market.
## **Problem Statement**
The Singapore real estate market is rapidly evolving, with increased competition from online platforms and disruptive business models. To stay ahead, property agents need more than just experience; they need data-driven insights. The HDB Resale Price Predictor Tool addresses this need by leveraging historical data and machine learning algorithms to predict future trends and prices in the HDB resale market.
## **Key Objectives**
1. **Empower Property Agents:** Equip agents with valuable data insights on HDB resale prices to enhance their decision-making and negotiation skills.
2. **Predict Pricing Trends:** Utilize advanced machine learning models to accurately forecast future resale price movements, enabling agents to anticipate market changes and advise clients accordingly.
3. **Increase Client Satisfaction:** Provide property agents with a powerful tool to guide clients on pricing strategies, maximizing transaction value and building long-lasting relationships.
4. **Identify Key Market Factors:** Uncover and highlight the most influential factors that drive HDB resale prices, enabling agents to tailor their advice to specific client needs and preferences.
5. **Mitigate Risk:** Assist agents in making informed decisions by providing data-backed assessments of potential risks and uncertainties in the HDB resale market.
6. **Optimize Investment Returns:** Empower property investors to make data-driven decisions that maximize their returns and minimize their risks.
7. **Stay Ahead of the Competition:** Provide agents with a competitive edge by offering a unique and valuable service that differentiates them from their peers.
8. **Foster Data-Driven Culture:** Promote a data-centric approach to real estate decision-making within the industry, leading to more informed and effective practices.
## Exploratory Data Analysis
(see slides / Tableau stories for charts)
- HDB resale prices saw a general upward trend over the past decade, with fluctuations influenced by various factors such as economic health of Singapore (i.e. interest rates, GDP growth, job market conditions, etc.), government policies (i.e. cooling measures, subsidies, incentives, etc.), supply/demand, and global events (e.g. pandemic, wars, etc.)
- There is significant disparity in resale prices across different towns. Proximity to CBD, transport hubs, schools, amenities (shopping malls, parks, recreational facilities) also influence property values
- Right-skewed distribution and concentration of flats in the middle price range suggest that HDB flats are generally affordable, with a smaller proportion of high-end flats available
- Floor area is the strongest predictor of resale price
- Flat type, flat model and location also significantly influence resale value
## **Machine Learning Models**
After experimenting with various models, the following top three models were chosen:
| Model       | Train RMSE  | Test RMSE   |  Train R²   | Test R²   | Model Run Time (s)   |
| ----------- | ----------- | ----------- |  ----------- | ----------- | ----------- |
| Random Forest Regressor | 16,789      | 26,227       | 0.986       | 0.966       | 52       |
| Extra Trees Regressor   | 14,894       | 26,421       | 0.989       | 0.966       | 56     |
| **XGBoost**   | **25,166**        | **27,074**       | **0.956**       | **0.964**      | **13**       |

XGBoost is selected as the preferred model due to its balance between speed, accuracy, and reliability. It consistently outperformed other models without overfitting. More details on the modelling and the features selected can be found [here](https://github.com/tanweijim/HDB-Resale-Price-Predictor/blob/main/notebook-datasprint.ipynb).
## **Key Insights**
Based on results by XGBoost, 
1. Flat Type: The larger the room type, the higher the price.
2. Floor level: The higher the floor level, the higher the price. Higher-level units generally offer unobstructed views and may benefit from improved ventilation due to stronger wind currents.
3. Certain towns: Bishan commanded a higher price, likely due to its proximity to top schools. Woodlands also featured strongly, likely due to its unique accessibility to Johor Bahru.
4. Flat models: Terrace flats, a limited and discontinued unit type in Singapore, command higher prices due to their unique design and scarcity. With only 285 units in existence, these flats represent a highly sought-after and exclusive housing option.
## **Future Development / Enhancements**
To enhance predictive accuracy, future iterations of the model will incorporate additional variables such as inflation rates, flat orientation, proximity to educational institutions, demographic trends, government policy changes, and the availability of nearby amenities like preschools and parks.
## **App Demo**
View App: HDB Resale Price Predictor (Coming Soon!)
