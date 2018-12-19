# Lab 1-1 and 1-2

### ADFS Sign On URL:

https://<span></span>2012r2std.oktaice.local/adfs/ls/IdpInitiatedSignOnPage


### ADFS IdP Config -  Okta:

  IdP Issuer URI: http://<span></span>2012r2std.oktaice.local/adfs/services/trust
  
  IdP Single Sign-on URL: http://<span></span>2012r2std.oktaice.local/adfs/ls
  
  
  
### ADFS - Okta Sign On URL:

https://<span></span>2012r2std.oktaice.local/adfs/ls/idpinitiatedsignon?loginToRp=OktaIce



# Lab 2-1 and 2-2

### Custom Username Format:

String.substringBefore(user.email, "@") + ".oktaice###@oktaice###.com"

# Lab 3-2
## Rebrand the Sign-In Widget Page and Login Container
### Step 2:
```html
<style>
  body {
    background-image: url("img/ice-cream-bg.jpg");
    background-size: cover;
  }
  #okta-sign-in .okta-sign-in-header {
    background-color: #FFFFEE;
  }
  #okta-sign-in .auth-content {
    background-color: #FF5C5C;
    color: #FFFFFF;
  }
  #okta-sign-in .okta-form-title{
    color: #FFFFFF;
  }
  #okta-sign-in .link.help.js-help{
    color: #FFFFFF;
  }
  #okta-sign-in .link.js-forgot-password{
    color: #FFFFFF;
  }
  #okta-sign-in .link.js-unlock{
    color: #FFFFFF;
  }
  #okta-sign-in .link.js-custom{
    color: #FFFFFF;
  }
  #okta-sign-in .link.js-help-link{
    color: #FFFFFF;
  }
</style>
```
### Step 4:
```css
var oktaSignIn = new OktaSignIn({
  baseUrl: orgUrl,
  logo: '/img/ice-logo.png'
});
```
## Customize the Sign-In Widget Settings
### Step 2:
```css
labels: {
  'primaryauth.title': 'Okta Ice SSO',
  'primaryauth.username.tooltip': 'Forgot your ID? Call <u>800-ICE-HELP</u>',
  'primaryauth.password.tooltip': 'Forgot your password? Call <u>800-ICE-HELP</u>'
},
helpLinks: {
  help: 'help/call.html',
  forgotPassword: 'help/forgot.html',
  custom: [
    { text: '1st access?', href: 'help/1st-time.html' }
  ]
},
features: {
  rememberMe: false,
  smsRecovery: true,
  selfServiceUnlock: true
}
```
