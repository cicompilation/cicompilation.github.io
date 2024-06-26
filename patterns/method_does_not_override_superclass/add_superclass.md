---
layout: page
---
## scribejava/scribejava 265.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/fernandezpablo85/scribe-java/src/main/java/org/scribe/builder/api/BiblioetecaApi.java:[12,3] method does not override or implement a method from a supertype 
```

### Code Change

---------------------

***src/main/java/org/scribe/builder/api/DefaultApi10.java***

```diff
+package org.scribe.builder.api;
+import org.scribe.extractors.AccessTokenExtractor;
+import org.scribe.extractors.BaseStringExtractor;
+import org.scribe.extractors.BaseStringExtractorImpl;
+import org.scribe.extractors.HeaderExtractor;
+import org.scribe.extractors.HeaderExtractorImpl;
+import org.scribe.extractors.RequestTokenExtractor;
+import org.scribe.extractors.TokenExtractorImpl;
+import org.scribe.model.OAuthConfig;
+import org.scribe.model.Token;
+import org.scribe.model.Verb;
+import org.scribe.oauth.OAuth10ServiceImpl;
+import org.scribe.oauth.OAuthService;
+import org.scribe.services.HMACSha1SignatureService;
+import org.scribe.services.SignatureService;
+import org.scribe.services.TimestampService;
+import org.scribe.services.TimestampServiceImpl;
+ /**
+* Default implementation of the OAuth protocol, version 1.0
+*
+* This class is meant to be extended by concrete implementations of the API,
+* providing the endpoints and endpoint-http-verbs.
+*
+* If your Api adheres to the 1.0 protocol correctly, you just need to extend
+* this class and define the getters for your endpoints.
+*
+* If your Api does something a bit different, you can override the different
+* extractors or services, in order to fine-tune the process. Please read the
+* javadocs of the interfaces to get an idea of what to do.
+*
+* @author Pablo Fernandez (copy of OAuth 1.0a), patched by Martin Vlcek (OAuth 1.0)
+*
+*/
+public abstract class DefaultApi10 implements Api
+{
+  /**
+* Returns the access token extractor.
+*
+* @return access token extractor
+*/
+  public AccessTokenExtractor getAccessTokenExtractor()
+  {
+    return new TokenExtractorImpl();
+  }
+   /**
+* Returns the base string extractor.
+*
+* @return base string extractor
+*/
+  public BaseStringExtractor getBaseStringExtractor()
+  {
+    return new BaseStringExtractorImpl();
+  }
+   /**
+* Returns the header extractor.
+*
+* @return header extractor
+*/
+  public HeaderExtractor getHeaderExtractor()
+  {
+    return new HeaderExtractorImpl();
+  }
+   /**
+* Returns the request token extractor.
+*
+* @return request token extractor
+*/
+  public RequestTokenExtractor getRequestTokenExtractor()
+  {
+    return new TokenExtractorImpl();
+  }
+   /**
+* Returns the signature service.
+*
+* @return signature service
+*/
+  public SignatureService getSignatureService()
+  {
+    return new HMACSha1SignatureService();
+  }
+   /**
+* Returns the timestamp service.
+*
+* @return timestamp service
+*/
+  public TimestampService getTimestampService()
+  {
+    return new TimestampServiceImpl();
+  }
+  
+  /**
+* Returns the verb for the access token endpoint (defaults to POST)
+*
+* @return access token endpoint verb
+*/
+  public Verb getAccessTokenVerb()
+  {
+    return Verb.POST;
+  }
+  
+  /**
+* Returns the verb for the request token endpoint (defaults to POST)
+*
+* @return request token endpoint verb
+*/
+  public Verb getRequestTokenVerb()
+  {
+    return Verb.POST;
+  }
+  
+  /**
+* Returns the URL that receives the request token requests.
+*
+* @return request token URL
+*/
+  public abstract String getRequestTokenEndpoint();
+  
+  /**
+* Returns the URL that receives the access token requests.
+*
+* @return access token URL
+*/
+  public abstract String getAccessTokenEndpoint();
+  
+  /**
+* Returns the URL where you should redirect your users to authenticate
+* your application.
+*
+* @param requestToken the request token you need to authorize
+* @return the URL where you should redirect your users
+*/
+  public abstract String getAuthorizationUrl(Token requestToken, String callback);
+  
+  /**
+* Returns the {@link OAuthService} for this Api
+*
+* @param apiKey Key
+* @param apiSecret Api Secret
+* @param callback OAuth callback (either URL or 'oob')
+* @param scope OAuth scope (optional)
+*/
+  public OAuthService createService(OAuthConfig config)
+  {
+    return new OAuth10ServiceImpl(this, config);
+  }
+}
++


```