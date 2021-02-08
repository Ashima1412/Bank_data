# Bank_data
# Case study - Domain – Banking Marketing

import pandas as pd
import numpy as np

df = pd.read_csv('bank_data.csv')
df.head()
list1=df.job.unique()
#print(df['job'])
while True:
    job_os = input('enter the job profile: ')

    if(job_os=='management' or job_os=='admin.'):
#if(df['age']>35):
            print('Congrats!! You are eligible for loan')
            
    elif(job_os=='END' or 'end'):
        break
    else:    
        print('Sorry!! you are not eligible')

###### Enhancement Codes #######
# Max and Min age for loan eligibility
ages = df.sort_values(by='age')
ages

# Dictionary of max min ages
#max_min_age = {"max": max(ages), "min": min(ages)}

print("Max age for loan eligibility ",df['age'].max())
print("Min age for loan eligibility ",df['age'].min())

Output:
enter the job profile: admin.
Congrats!! You are eligible for loan
enter the job profile: end
Max age for loan eligibility  80
Min age for loan eligibility  19
