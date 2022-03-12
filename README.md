# React에서 환경변수 설정하기

## 환경변수 파일 정의

### `.env`

```
REACT_APP_NAME = "My Awesome Homepage"
```

### `.env.development`

```
REACT_APP_URL="https://dev.endpoint.com/"
REACT_APP_API_ENDPOINT = "https://api-dev.endpoint.com/"
```

### `.env.testing`

```
REACT_APP_URL="https://testing.endpoint.com/"
REACT_APP_API_ENDPOINT = "https://api-testing.endpoint.com/"
```

### `.env.staging`

```
REACT_APP_URL="https://staging.endpoint.com/"
REACT_APP_API_ENDPOINT = "https://api-staging.endpoint.com/"
```

### `.env.production`

```
REACT_APP_URL="https://endpoint.com/"
REACT_APP_API_ENDPOINT = "https://api.endpoint.com/"
```

## package.json에 환경에 맞는 빌드 스크립트 추가

```
"scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "build:testing": "env-cmd -f .env.testing react-scripts build",
    "build:development": "env-cmd -f .env.development react-scripts build",
    "build:staging": "env-cmd -f .env.staging react-scripts build",
},
```
