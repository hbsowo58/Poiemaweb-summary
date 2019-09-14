webpack은 설정의 연속, 바벨 로더에 대한 옵션 (babel-preset-env)=> plugin들의 모음



['@babel/preset-env',{ target:{browser:['last 2 chrome versions'],}}] 크롬 최근2버전만



github/browserslist 가면 옵션 보기 가능

last 1version

1%



debug:true 이런것도 있음



plugins: [], 그냥 플러그도 있네(확장프로그램)

new webpack.LoaderOptionsPlugin({ debug: true }),

실무코드에 열개정도 껴있을 수 있음



target vs currentTarget 차이?