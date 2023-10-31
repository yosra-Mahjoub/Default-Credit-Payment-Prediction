# Default Credit Payment Prediction

Predicting credit card payment defaults using machine learning models.

## Table of Contents

- [About](#about)
- [Dataset Information](#dataset-information)
- [Input Parameters](#input-parameters)
- [Label](#Label)
- [Modeling](#modeling)

## About

This project focuses on predicting credit card payment defaults using a dataset that includes information on demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005. The goal is to build and evaluate machine learning models that can determine whether or not a customer will default on their credit card payment in the next month.

## Dataset Information

The dataset contains 25 variables, including client IDs, credit amounts, gender, education, marital status, age, payment history, bill amounts, and previous payment amounts. The target variable, `default.payment.next.month`, is binary, with 1 indicating a customer will default and 0 indicating they will not.

## Input Parameter

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `LIMIT_BAL` | `float64` | **Required**. Amount of given credit |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `SEX` | `int64` | **Required**. Gender (1=male, 2=female) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `EDUCATION` | `int64` | **Required**. (1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `MARRIAGE` | `int64` | **Required**. Marital status (1=married, 2=single, 3=others) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `AGE` | `int64` | **Required**. Age in years |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_0` | `int64` | **Required**. Repayment status for 1st month(-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_2` | `int64` | **Required**. Repayment status for 2nd month(-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_3` | `int64` | **Required**. Repayment status for 3rd month(-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_4` | `int64` | **Required**. Repayment status for 4th month(-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_5` | `int64` | **Required**. Repayment status for 5th months(-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_6` | `int64` | **Required**. Repayment status for 6th month(-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above) |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `BILL_AMT1` | `float64` | **Required**. Amount of bill statement for 1st month|

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `BILL_AMT2` | `float64` | **Required**. Amount of bill statement for 2nd month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `BILL_AMT3` | `float64` | **Required**. Amount of bill statement for 3rd month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `BILL_AMT4` | `float64` | **Required**. Amount of bill statement for 4th month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `BILL_AMT5` | `float64` | **Required**. Amount of bill statement for 5th month|

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `BILL_AMT6` | `float64` | **Required**. Amount of bill statement for 6th month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_AMT1` | `float64` | **Required**. Amount of due payment recieved for 1st month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_AMT2` | `float64` | **Required**. Amount of due payment recieved for 2nd month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_AMT3` | `float64` | **Required**. Amount of due payment recieved for 3rd month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_AMT4` | `float64` | **Required**. Amount of due payment recieved for 4th month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_AMT5` | `float64` | **Required**. Amount of due payment recieved for 5th month |

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `PAY_AMT6` | `float64` | **Required**. Amount of due payment recieved for 6th month |

## Label

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `default.payment.next.month`      | `int` | **One** if customer will default otherwise **Zero**|

The output is a binary classification prediction, as described, indicating whether a customer is likely to default on their credit card payment.

## Modeling

To train and test the dataset, the following machine learning models are implemented:
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Random Forest
- Decision Tree
- AdaBoost

