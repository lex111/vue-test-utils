## setValue(value)

Этот метод — псевдоним следующего кода.

```js
wrapperArray.wrappers.forEach(wrapper => wrapper.setValue(value))
```

<<<<<<< HEAD
- **Arguments:**
  - `{any} value`

- **Example:**
=======
- **Принимает:**
  - `{any} value`

- **Пример:**
>>>>>>> 1998c5341065fbe6a5e6bc6310ccaa5a9e604fd1

```js
import { mount } from '@vue/test-utils'

const wrapper = mount({
  data () {
    return {
      t1: '',
      t2: ''
    }
  },
  template: `
    <div>
      <input type="text" name="t1" class="foo" v-model="t1" />
      <input type="text" name="t2" class="foo" v-model="t2"/>
    </div>`
})

const wrapperArray = wrapper.findAll('.foo')
expect(wrapper.vm.t1).to.equal('')
expect(wrapper.vm.t2).to.equal('')
wrapperArray.setValue('foo')
expect(wrapper.vm.t1).to.equal('foo')
expect(wrapper.vm.t2).to.equal('foo')
<<<<<<< HEAD
```
=======
```
>>>>>>> 1998c5341065fbe6a5e6bc6310ccaa5a9e604fd1
