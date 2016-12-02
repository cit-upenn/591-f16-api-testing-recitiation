## Obtain Training Data from Twitter
### Install Package
Twitter4J API: [http://twitter4j.org](http://twitter4j.org)
1. Go to the Twitter4J homepage 
2. Download twitter4j-4.0.4.zip 
3. Locate twitter4j-core-4.0.4.jar package inside the lib folder 
4. Copy the jar to your a folder named lib working directory 
5. Add it to your Eclipse project
6. Fill in TwiterAPIConfig.java with your account info

### Obtain API credentials
1. Link a mobile number to your twitter account 
2. Go to [http://dev.twitter.com](http://dev.twitter.com) -&gt; My Apps -&gt; Create New App
3. Set the keys and tokens using the info in Keys and Access Tokens

### Clean Tweet Data
1. Look in the files insrc/twitter directory and ScrapeRunner.java
2. The cleanTweet method needs to be implemented.
Tip: Try with 10 initially due to rate-limit. Limitations of 100 tweets/query, no tweets older than a week, 450 tweets/15 mins


###Example
<span style="color:red">Own a bike? Out of 2000+ options for a Bike Pump on https://t.co/TAmOOP4QS1, I finally found the perfect one :) https://t.co/8xF32LqfUf #Ad  

<span style="color:green"><b> Own a bike Out of  options for a Bike Pump on  I finally found the perfect one </b><span>

<span style="color:red">RT @LiamPayne: @KimKardashian hey Kim what's your favorite song on up all night :)</span>

<span style="color:green"> <b>hey Kim whats your favorite song on up all night</b></span>

## Train Watson using Twitter Data

Watson NLC API: [http://ibm.com/watson/developercloud/natural-language-classifier/api/v1](http://ibm.com/watson/developercloud/natural-language-classifier/api/v1)

Guidelines for Training Data: [http://www.ibm.com/watson/developercloud/doc/nl-classifier/data_format.shtml](http://www.ibm.com/watson/developercloud/doc/nl-classifier/data_format.shtml)

### Install Package
1. Go to [http://github.com/watson-developer-cloud/java-sdk](https://github.com/watson-developer-cloud/java-sdk) 
2. Download the JAR with dependencies 
3. Copy the jar to your a folder named lib working directory
4. Add jar to Eclipse
5. Fill in TweetClassifier.java with your account info 

###Obtain API credentials
1. Make account at [http://bluemix.net](http://bluemix.net) 
2. Launch Bluemix 
3. Create Application -&gt; Watson -&gt; Natural Language Classifier 
4. Press Create in the bottom right 
5. Select Server Credentials -&gt; View Credentials 
6. Copy username and password into WatsonApiConfig.java

### Use Tweet Data with Watson
1. Create tests for WatsonJSONParser
2. Implement JSONParser to extract only the field we need
3. Create a job for the data scraped from Twitter
4. Use the printJobStatus method to query ifnromation about that status 
5. In the meantime, checkout the job that was run last night
