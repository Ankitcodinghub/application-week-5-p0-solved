# application-week-5-p0-solved
**TO GET THIS SOLUTION VISIT:** [Application Week 5 P0 Solved](https://www.ankitcodinghub.com/product/application-p0-solved-5/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124728&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Application Week 5 P0 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
Portfolio Optimization MA-

Application of Matlab for Finance

Week 5

Portfolio Optimization MA-

I MA-Crossover Trading Strategy

I Trading Strategy Returnshttps://.com

I Drawdown Curve (Optional)

Add Obtain Data

from External Source: FRED

I Today, we will use Matlab to retrieve data from external sources.

I Download the historical price of S&amp;P500 index for

Bank of St.Louis (FRED): https://.comI website: https://research.stlouisfed.org/fred2/

I code fred is the build-in connection from Matlab to

FRED I ensure the ’Datafeed’ package is properly installed

Portfolio Optimization MA-

I Other connections include blp for Bloomberg, ravenpack for RavenPack News Analytics, both of which require information on relevant terminals.

Obtain Data from External Source: FRED

1

c = fred; % connect to FRED

2

ticker = ‘SP500’; % define the ticker of the stock

Assignment Project Exam

5 Help3 start_date = ‘2008/01/01′;

6 data = fetch(c,ticker,start_date,end_date); 7 close the connection close(c) %

https://.com

I Function fetch() retrieves data for a defined stock ticker from connection c within specified dates

I The information is stored in aAdd structure variable called data.

I Accessing the fields of data using dot (.):

I data.Data: the Data field of structure variable data

I data.SeriesID: the SeriesID field of structure variable data

I Always remember to close the connection close(c).

Clear Data with Missing Observations

Consider a (T × N) price matrix with T observations on N stocks.

I We want to delete the days if any stock price on that day is missing. I isnan(p) returns logical output 1 if observation p(t,n) is NaN

I missing = any(isnan(p),2) returns logical output 1 if any stock on datehttps://.comt is NaN.

I That is, on row t, if any p(t,n) == NaN, then missing(t,1)=1.

I The corresponding row t with missing==1 in the original data is deleted by settingAdd =[];

I Note: any(..,2) specifies the operation is on the row dimension.

1

%% Clear missing observations

2

missing = any(isnan(data.Data),2);

3 data.Data(missing,:)=[];

1 %% Read Data &amp; Calculate Returns

2 spy_t = data.Data(:,1); % read serial timevalue number

4 spy_t_str = datestr(spy_t,’dd/mm/yyyy’) 5 % read historical price

Assignment Project Exam

Help6 spy_p = data.Data(:,2);

7 % calculate continuous return

8 spy_lnret = tick2ret(spy_p, spy_t, ‘continuous’);

9 10 figure 11

I column 1 and price in column 2.

I The serial datetime number records time in numerical format, which is necessary for time series analysis and figure plot.Add

I tick2ret() calculates the continuous return of spy_p with time sequence spy_t.

I The histogram shows that the return distribution is rather symmetric.

Calculate Moving-Average Series

I A moving average at time t with n-day window is the arithmetic average of price from t − n + 1 to t: MA_21

2 sma_st = tsmovavg(spy_p, ‘s’, 21, 1);

3 % long−term simple moving average 126 days https://.com4 sma_lt = tsmovavg(spy_p, ‘s’, 126,1);

I tsmovavg() calculates the simple moving average,’s’, on the column price vector, spy_p, for 21 days and 126 days.

I The last inputAdd 1 specifies it is the column matrix dimension. I Other MA calculation includes exponential, ‘e’, triangular, ‘t’.

I In finance, we use working day counting, instead of calender days.

I 21 days: 1 month

I 126 days: 6-month

I 252 days: 1 year

Plot the MA time series

1 clf % clear the previous figure

Assignment Project Exam

Help2 figure

3 plot(spy_t,spy_p,’b−−’,spy_t,sma_st,’g’,spy_t,sma_lt,’r’) 4 legend(‘SPY Price’, ‘SMA(21)’, ‘SMA(126)’, …

‘Location’,’northwest’)

5 dates_limits = [min(spy_t), max(spy_t)];

6 xlim(dates_limits)% set the x limits

datetick(‘x’) %

8 ylabel(‘Price’)

9 title(‘MA−CrossOver Trading Strategy’)

I plot(x,y1,x,y2,x,y3..)Add plots various times series on the same graph, x,y1,y2,y3 are of the same length.

I ‘b’,’g’,’r’ specify corresponding line color.

I ‘−−’ specifies line type: dashed line.

https://.com

Add

The MA Cross Trading Strategy

I The MA cross trading strategy uses technical analysis on past prices

I Buy signal when the short-term trend cross-up long-term trend from bottom → buy and hold position when sma_st&gt;sma_lt

I Sell signal when short-term trend cross-down long-term trend from top → short sell position when sma_st&lt;sma_lt

https://.com

Add The MA

Cross Trading Strategy

I sma_st &gt; sma_lt gives logical output 1 when it is true.

I position=1https://.com*2−1=1 after a uplifting buy cross (sma_st&gt;sma_lt)

I position=0*2−1=−1 after a death sell cross (sma_st&lt;sma_lt)

I Note: Code position=(sma_st&gt;sma_lt) means a passive trading strategy that you buy the stock after a buy signal and sell theAdd

underlying after a sell signal: position=0 when sma_st&lt;sma_lt.

I Note: Code position=(sma_st&gt;sma_lt)*2−1 is the relative active trading strategy that you engage in short selling activity after a selling signal by setting position =−1 when sma_st&lt;sma_lt. SubPlot Assignment Project Exam He1 subplot(2,1,1) lp

2 plot(spy_t,spy_p, spy_t, sma_st, spy_t, sma_lt)

3 subplot(2,1,2)

4 plot(spy_t, position,’LineWidth’,2)

I subplot(m,n,p)https://.comcreate a figure with various plots I The actual plot codes of plotting comes after subplot(m,n,p). I m,n define the plots layout structure: m rows n column panels.

Add I p defines which sub-plot panel is defined in the following codes.

I In above code, we create a figure with 2×1 plot panels

I the first panel plots the price and moving-average.

I the second panel plots the position. Plot

the Trading Position

1 figure

2 subplot(2,1,1)

3 plot(spy_t, spy_p, spy_t, sma_st, spy_t, sma_lt) 4 legend(‘SPY Price’, ‘SMA(21)’, …

tion’,’northwest’)

5 dates_limits = [min(spy_t), max(spy_t)];

6 xlim(dates_limits)

78 datetick(‘x’)

9

10 plot(spy_t, position,’LineWidth’,2) 11 xlim(dates_limits)

12 datetick(‘x’)

Plot the Trading Position

https://.com

Add

Calculate Returns

1 %% Calculate returns

2 %daily and cumulative return on the MA strategy

3

strategy_ret = position(2:end).*spy_lnret;

4

cumret_strategy = exp(cumsum(strategy_ret));

5 % cumulative return on market benchmark

6 cumret_market = exp(cumsum(spy_lnret));https://.com

I strategy_ret is the daily return based on the trading strategy I (2:end) as the 1st-day has no return yet;

Add I note: we use element-by-element multiplication with the dot (.).

I Use cumsum as we work with ln return; and use the exp to convert back to cumulative simple return for comparison.

I The market benchmark assumes a buy and hold trading strategy. Plot the Cumulative Return

ssignment Project Exam Help figure

2 plot(spy_t(2:end), cumret_strategy,’b’);

3 hold on % hold on the previous plot

4 plot(spy_t(2:end), cumret_market,’g’);

5 legend(‘Strategy’,’Market’)

6 dates_limits = [min(spy_t), max(spy_t)];

8 datetick(‘x’)

9 ylabel(‘Cumulative Return ‘)

I hold onAdd retains plots in the current axes so that new plots added to the axes; otherwise, the new plots will overwrite the existing ones.

I spy_t(2:end) as we plot returns now.

I From the plot, it is clear that the trading strategy outperforms the market itself.

Plot the Cumulative Return

https://.com

Add

Annual Summary Statistics

Assignment Project Exam

Help1 %% Calculate Annual Return

2 annual_ret = mean(spy_lnret) * 252;

3 annual_std = std(spy_lnret) * sqrt(252);

4 % assuming the rf = 0.03

5 sharpe_ratio = (annual_ret − 0.03) / annual_std; 6

%combine

7 results togethe to display

8 res = [annual_ret,annual_std,sharpe_ratio];

9 disp([‘The annual return, stdeve and Sharpe Ratio are: …

‘,num2str(res)])

I Annualise daily ln return by multiplying 252, the number of tradingAdd days in a year.

I Annualise standard deviation by multiplying square root of 252.

I Assume a relevant annual risk-free rate to calculate Sharpe ratio.

Construct Drawdown Curve

Assignment Project I A drawdown curve evaluates the performance of a trading strategyExam Help against its own best performance. DDt = HWMRt−Rt

I At t = 0, set a high water mark (HWM) = 1.

I Athttps://.comt = 1, the trading strategy makes a return = 1.5

I 1.5 &gt; HWM =1 → new HWM =1.5, and drawdown = 0

I At t = 2, the trading strategy makes a return, but lower = 1.2

I 1.2 &lt; HWM =1.5 → HWM =1.5 stays the same

Add I drawdown = (1.5-1.2)/1.2 =0.25

I A peak in the drawdown curve is the maximum loss in the profits from the highest profit point in history Construct Drawdown Curve

1 %% Calculate the Drawdown Curve 2 % set HMW = 1 for start with.

3 high_water_mark = 1;

4 T = length(cumret_strategy);

m

6 for t = 1:T

7 if cumret_strategy(t) &gt; high_water_mark

8 high_water_mark = cumret_strategy(t);

9 end

powcoderdrawdown = (high_water_mark − …

cumret_strategy(t))/cumret_strategy(t);

11 dd_curve(t) = drawdown;

12 end

Plot the Drawdown Curve

Take Away

I Extract data from external resources and how to clear data.

I Calculating moving average and construct trading position.

I Calculate returns, cumulative returns and annualise relevanthttps://.com summary statistics

I The concept of drawdown curve in asset manager performance

evaluationAdd
