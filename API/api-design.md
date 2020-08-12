# API Design Guidelines
## General Guidelines
### GD 1 - Keep your apis in a dedicated subdomain
If you are running your API behind a api gateway you should create a dedicated subdomain for it (e.g. api. or api-gateway)
```yaml
https://api.domain.de/
```

### GD 2 - Define your domain model upfront
If you are running more than a hand of api you should think about clustering them into separate domains or finegrained subdomains.
```yaml
https://api.domain.de/sales/
https://api.domain.de/marketing/online/
```

### GD 3 - Keep your API names consistent
Try to create object oriented and resource focused api models. You should name your apis following a concrete convention. So you could name your apis starting with the main resource you want to handle following by the word "-management".
```yaml
https://api.domain.de/sales/customer-management/
https://api.domain.de/marketing/online/newsletter-management/
```

### GD 4 - Define your APIs resource oriented
APIs are resource oriented integrations - so please do not define APIs on a functional base

```yaml
## bad - try to not name your api path like an action
POST https://api.domain.de/marketing/online/newsletter-management/sendMail 

## good - the resource is of the type mail and the POST methode indicates that you want to create one
POST https://api.domain.de/marketing/online/newsletter-management/mail    
```


## API Elements

### General API Description

```yaml
openapi: "3.0.1"
info:
  title: "Customer Data API"
  version: "1.0.0"
  description: "Using the Customer Data API you can easily manage your customer data ..."
```

### Path Design

### Query Parameters

### Request

### Response

### Status Code

## Security

### JWT Token

### Auth Endpoints
