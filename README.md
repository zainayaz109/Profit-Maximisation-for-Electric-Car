# Profit-Maximisation-for-Electric-Car

The goal of the project was to generate a profit with price arbitrage by using an electric car as energy storage. In the attached python file there is a data frame that contains electricity day-ahead prices (in €/MWh) of 2021. Suppose you can buy and sell electricity at those rates and use the battery of an electric car as storage, the goal is to make as much money as possible from price arbitrage.

## Data
The dataset is private so it cannot be shared publically.

## Technical inputs/boundaries:
• Simulate process of buying and selling electricity over a whole year, start at January 01 00:00 with a full battery

    • Maximise profit over the whole year
    
• Battery size (maximum storage) is 50 kWh

• It is possible to either charge or discharge the battery with a maximum of 10 kWh per hour, take the price at the beginning of the hour to calculate profits (e.g. battery is charged with 30 kWh and price at 6pm is 0.30 cents/kwH, you can either buy 10 kWh for 3€ and have 40 kWh or sell 10 kWh for 3€ and have 20 kWh)

    • Note that there are hours with negative electricity costs, so you can actually gain money while charging the car

• Charging and discharging is only possible at night between 6pm and 8am, during the day no charging is possible and the car loses 10 kWh state of charge due to driving

    • SOC at 6pm = SOC at 8am – 10 kWh
    
• Minimum of 80% battery charge (40 kWh) is required in the morning at 8am, other than that there are no boundaries (full discharge during the night is possible as long as it’s charged back to at least 40 kWh at 8am)

• Profits are accumulated over the whole year, prices are known in advance for any given hour