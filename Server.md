# 개발 환경
 - `ASP.NET` (.NET Core 3.1)
 - `Template` (WebAPI)

# 배포 환경
 - 배포 환경 구성
 - `Windows Server 2016`
 - `IIS`

# 솔루션 구조
- MaaS.sln
    + Common
    + WebAPI
        * Attribute : API의 속성 관련 정의
        * Controllers : API Route, 주석을 통한 Swagger연동
        * Database : Model의 DB관련 정의
        * Middleware : ASP의 Custom Middleware
        * Models : Controller에서 다룰 Model
        * Request : Controller에서 다룰 요청
        * Settings : ASP 구동시 로딩할 Config 변수
        * Map(`Web`) : ASP에서 호스팅 할 Map View

# 참조 구조
* MaaS
    + WebAPI
        - Common
        - Map

# 코딩 컨벤션
- 기본 적인 컨벤션은 `Cammel`
- 멤버 변수 접두사로 `_`추가

# 빌드 방법
```
dotnet build
dotnet build --runtime win10-x64
```
```
dotnet publish -c Release
dotnet publish -c Release --runtime win10-x64 --self-contained true
```
