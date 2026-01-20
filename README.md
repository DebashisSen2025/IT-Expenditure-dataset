# IT-Expenditure-dataset
Monthly Variance Analysis: IT Expenditure Insights Used Python &amp; Seaborn to visualize Actual vs Plan and Forecast variances, highlighting overspending, efficiency gains, and opportunities for better forecasting. Clear bar plots and storytelling turned raw data into actionable insights.
print("--- Monthly Variance Plots ---")

# Plotting Actual vs Plan Variance for Month
fig, axes = plt.subplots(1, 2, figsize=(16, 6))
sns.barplot(x=top5_month_plan_high.index, y='Actual vs Plan Variance', data=top5_month_plan_high, ax=axes[0], palette='viridis')
axes[0].set_title('Top 5 Months: Actual vs Plan Variance')
axes[0].set_xlabel('Month')
axes[0].set_ylabel('Actual vs Plan Variance')
axes[0].ticklabel_format(style='plain', axis='y')

sns.barplot(x=top5_month_plan_low.index, y='Actual vs Plan Variance', data=top5_month_plan_low, ax=axes[1], palette='plasma')
axes[1].set_title('Bottom 5 Months: Actual vs Plan Variance')
axes[1].set_xlabel('Month')
axes[1].set_ylabel('Actual vs Plan Variance')
axes[1].ticklabel_format(style='plain', axis='y')
plt.tight_layout()
plt.show()

# Plotting Actual vs Forecast Variance for Month
fig, axes = plt.subplots(1, 2, figsize=(16, 6))
sns.barplot(x=top5_month_forecast_high.index, y='Actual vs Forecast Variance', data=top5_month_forecast_high, ax=axes[0], palette='viridis')
axes[0].set_title('Top 5 Months: Actual vs Forecast Variance')
axes[0].set_xlabel('Month')
axes[0].set_ylabel('Actual vs Forecast Variance')
axes[0].ticklabel_format(style='plain', axis='y')

sns.barplot(x=top5_month_forecast_low.index, y='Actual vs Forecast Variance', data=top5_month_forecast_low, ax=axes[1], palette='plasma')
axes[1].set_title('Bottom 5 Months: Actual vs Forecast Variance')
axes[1].set_xlabel('Month')
axes[1].set_ylabel('Actual vs Forecast Variance')
axes[1].ticklabel_format(style='plain', axis='y')
plt.tight_layout()
plt.show()
