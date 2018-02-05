# mobx

@observer观察者 当状态发生变化时，组件也会做相应的更新

@observable被观察者 观察类的值

@action 强制使用action来修改状态，唯一能改变state的方法

state 最基础的数据

computed values 纯函数从state中派生来的



store/page.js

```
import {observable} from 'mobx'
class Page {
  @observable current = 'home'
}
export default new Page()
```

store/index.js

```
import StorePage from './page'
export default {
  StorePage
}
```

components/CompetingData/index.js

```
@inject('StorePage)
compoentWillMount() {
  this.props.StorePage.current = 'comoeting'
}
```

```
<ul>
   {(this.checked('a')||this.checked('b'))&&(
     <li data-active={ current === 'comoeting'}>
   ) )}
</ul>
```





ES6允许使用反引号  ’  来创建字符串，这种方法创建的字符串里面可以包含${vraible}

console.log('your num is ${num}')

```
const Page = Styled.div`
  background: #010206 url(${ bg }) center 0;
  background-size: cover;
  min-height: 100%;
  padding: 0 15px;
  padding-bottom: 12px;
  min-width: 1200px;
`

```









QN2332060722













