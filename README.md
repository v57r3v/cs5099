java c
STATS 763 
STATISTICS 
Advanced Regression Methodology 
FIRST SEMESTER, 2019
1. (24   marks;   4   each)   Deﬁne or explain briefly in   the context of this   class
(a)   facetting
(b)   ridge regression
(c)   collider
(d)   apparent error
(e)   competing risks
(f)   sparse   matrix
2. (24   marks) You have data from a series of   randomised clinical trials (experiments) of   related   drugs to   prevent   heart   attacks:    that   is,   people   are   recruited   into   an   experiment   and then   randomly assigned to one of two treatments.   Y   is a binary variable indicating heart attack,   D   is a factor variable with m   +   1 levels 0,   1, . . . ,   m indicating which drug the person received   (with D   = 0 for no treatment), and G   is a factor variable with k   levels 1,   2, . . . , k   indicating   which trial the person was in.   You ﬁt   two models
model1      <- glm(Y~D, family=binomial(log))
model2      <- glm(Y~D+G, family=binomial(log))
(a)   (4   marks) What is the interpretation of   the coefficient labelled D1 in the   output   of   model   1?
(b)   (4   marks) What is the interpretation of   the coefficient labelled D1 in the   output   of   model   2?
(c)   (8   marks) Explain why the coefficient labelled D1 in model 2 has a causal interpretation,   but the coefficient labelled G3   does not have   a   causal   interpretation.
(d)   (4   marks)   What is the variance function for this generalised linear model?
(e)   (4   marks)   Does the link function we are using give the natural parameter for the expo-   nential   family?
3. (24   marks) A   popular model for   rainfall combines a logistic   regression for   whether rain occurs   or   not   and   a   Gamma   regression   for   the   amount   of rain   if any   occurs.      Consider these two   models   for   rainfall   amount   ﬁtted   to   daily   data   from   Auckland,   where   Amount   .   mm   .       is   the   amount of   rain in millimetres, rain indicates whether there was rain on that day, and month   is the month   (1–12)
model0    <-glm(formula = Amount. mm.~1, family = Gamma(log), data = auck, subset=rain==TRUE)
model1<-glm(formula = Amount . mm . ~sin(month * 2 * pi/12) +
cos(month      *      2    *   pi/12),      family      =      Gamma(log),   data      =    auck,    subset=rain==TRUE)
model2<-glm(formula = Amount. mm.~factor(month),
family      =      Gamma(log),      data      =    auck,    subset=rain==TRUE)The   likelihood   ratio p-value   testing   model   2   against   model   1代 写STATS 763 Advanced Regression Methodology FIRST SEMESTER, 2019Python
代做程序编程语言   is   0.056,   the   likelihood   ratio   p-value testing model   1 against model 0   is   0.047, the   AIC   for   model   0   is   2478,   the   AIC   for   model   1 is 2473, and the   AIC   for   model   2   is   2468.
(a)   (4   marks)The intercept in model 0 is   1.86.   What is the interpretation of this value?   (b)   (5   marks)   Is model 2 nested in model   1?   Explain.
(c)   (6   marks) Which model would you expect to have lowest out-of-sample prediction error   for the amount of rain on days when there was rain?   Explain.
(d)   (4   marks)   The dispersion parameter in model 0 is   estimated   as   2.35.   What,   according   to the model, is the variance of   the amount of rain on days when   there   is   rain?
(e)   (5   marks)   An   alternative   model   is   a   (Normal)   linear   model   for   the   logarithms   of the   non-zero rain amounts.   How would the interpretation of the coefficients   for   this   model   difer from the Gamma model?
4. (24   marks) Researchers studying autism spectrum disorder (ASD) were looking for biochem-   icalways   to diagnose ASD   in infants   where current   diagnostic   methods   can’t   be   used   reliably.   They measured concentrations of 87 chemicals in the blood of 60 children (not infants) diag-   nosed with ASD and 60 control children who did not have any diagnosis   of   ASD   or any   other   neurological or psychiatric illness.   They used the lasso   (L1-penalised   maximum   likelihood)   to ﬁt a logistic regression   model   predicting   ASD   diagnosis   from the   87   predictor   variables.   Predictions from the model had 95% sensitivity and 95%   speciﬁcity
(a)   (6   marks)   Write   down   the   objective   function   that   is   being   minimised   (you   can   write   L(β;   Y) for   the   binomial   likelihood   at   parameter   values   β).
(b)   (6   marks)   Give two advantages that are relevant to this analysis of   the lasso/L1    penalty   approach over stepwise logistic regression
(c)   (6   marks)   The size of the penalty was chosen   by   crossvalidation.    Briefly explain what   cross-validation is.
(d)   (6   marks)   In the population as a whole, about   1.5% of children end   up   diagnosed   with   ASD.   Assuming that the   sensitivity   and   speciﬁcity   are the   same   in the   population   as   in the experimental sample, what   proportion   of   those   predicted   by   the   model   to   have   ASD would end up with a diagnosis of ASD by existing criteria.







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
