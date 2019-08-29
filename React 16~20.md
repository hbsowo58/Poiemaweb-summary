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





- Webpack에서 반드시 알아야할 Concepts 들 5가지가 무엇인가요?

  mode, entry, module, plugins, output

- React의 Form태그 안에 속성 2가지 (   )와 (   )는 세트로 속성에 넣어주어야 한다. 만약 한가지만 넣을거면 defaultValue만 사용.

  value, onChange

- werbapck-dev-server , react-hot-loader 는 무엇을 하나요?

  werbapck-dev-server : 내 컴퓨터가 서버가 되어서 동작하게끔 만들어줌. locathost주소로 작동하게끔

  react-hot-loader : 코드 수정하면 화면이 자동으로 바뀌게끔 만들어줌.

  **webpack.config.js 파일이 바뀌게되는경우 다시 npx webpack-dev-server —hot 해주어야한다.

- plugin들의 모음을 무엇이라 하는가?

  preset

- @babel/preset-env에서 targets의 browsers속성에 다음과 같이 주면 어떻게 되나?? cover 99.5% , > 5% in US  targets

  브라우저의 99.5% 를 커버하겠다(지원) , US에서 사용하는 비중이 5% 이상의 브라우저들만 지원하겠다.

- Q. preset은 (	)들의 모음이다.

  plugin

- Q. @babel/preset-env은 어떤 설정을 할수 있나

  지원할 브라우저 환경을 설정 할수있다.

- Q. onChange를 사용하지 않을때는 (	)을 사용해야 한다.

  defaultValue

- Q. webpack-dev-server를 사용하는 이유

  webpack.config.js를 바탕으로 로컬 환경에서 서버를 구동시켜준다.

- Q. react-hot-loader는 어떤걸 도와주나요

  코드의 변경점(수정)을 확인하고 자동 빌드한다.

- babel을 이용하여 브라우저의 지원 범위를 설정하고 싶을 때 어떻게 하면 되는가?

  webpack.config.js 파일에서 module -> rules -> options -> presets -> @babel/preset-env -> targets -> browers

- event 객체의 프로퍼티인 currentTarget 과 target의 차이는???

  ```
    <div onclick="checkTarget();">
         <span>test</span>
       </div>
  
    function checkTarget(event) {
      var ele = event.currentTarget;
      console.log(ele);
    }
  ```

  - event.target // 클릭된 span 태그를 반환
  - event.currentTarget // 이벤트가 바인딩된 div 요소를 반환

- React 개발단계에서 jsx 파일의 코드 변화를 감지하여 즉시 변경사항을 반영하여 주는 역할을 하는 것은?

  Webpack dev server 와 react-hot-loader

- plugin들의 모음을 [ ]이라고 한다.

  preset

- 예전 브라우저도 환경에 맞게 알아서 코드를 변환시켜주는 모듈에 이름은?

- `webpack.config.js`에 `preset-env` 설정에서 지원 브라우저를 설정할 수 있다. 지원하는 브라우저를 설정해야하는 이유는?

  지원하는 브라우저를 상세히 적지 않으면 지원하지 않는 브라우저에 대한 코드들도 생겨나서 코드량이 많아져서 점점 더 느려진다.

- react에서 `form`을 쓸 때 `value` 속성과 `onChange` 속성은 세트이다. 두개를 같이 안 쓰면 에러가 나는데 두개를 대체할 수 있는 속성은?

  defaultValue

- react에서 실시간으로 코드를 적용하려면 어떤 모듈을 써야하나?

  `webpack-dev-server`와 `react-hot-loader`

- Webpack Dev Server를 사용할 때 log에 `[HMR]`와 `[WDS]`의 풀네임은?

  - [HMR] = Hot Module Replacement
  - [WDS] = Webpack Dev Server

