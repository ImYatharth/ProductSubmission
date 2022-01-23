# ProductSubmission
**Name**: Yatharth Champaneria <br>
**Mail**: ychampaneria3@gmail.com <br>
**Phone**: 8000334422

## Product Analyst Screening Problem Submission

Looking at the given Computation capacity data, we can assume that the current reserved capacity is 4000 units. The timestamps have been spread out throughout the 24 hours of the day with a lot of missing timestamps in between indicating a generally spread operation of the machine. 

For our problem-solving purpose, I have taken the assumption that any value which exceeds our set assumption capacity will cost 2.5x the usual one. The usual approach will be to set the limit to a very high value so as to minimize the excess 2.5x expenditure. But that would ultimately result in many values falling in the less than the reserved capacity zone, which would also not optimize our solution because then a lot of wasteful capacities will occur.

A normal approach would be trying out different values in both the greater than 4000 and less than 4000 so as to determine which value is resulting in minimum expenditure. Since I have assumed the 2.5x value, My optimal reserved capacity comes out to be 5540 units. 

This value is based on the given data and the 2.5x assumption. The algorithm by which I reached to this solution can be found on the link below:
<a href="https://drive.google.com/file/d/1WW0dZa8AOL3UcQI-5o2waf29JdbDKYpa/view?usp=sharing">Screenshot 2022-01-24 at 12.30.31 AM.png</a>


## Algorithm
```
for(int i=0;i<=13760;i++)
{
    sum=0;
    for(int j=0;j<=21;j++)
    {
        if(x[j]>i)
        sum=sum+i+(x[j]-i)*2.5;
        else
        sum=sum+i;
    }
    if(sum<csum)
    {
        csum=sum;
        n=i;
    }
}
```
**The array represents all the used capacities.**
