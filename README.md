# my_js_test
my_js_test (travail OC Informatique)



1.
// la VARIABLE a étant une expression regulier
var a = /^Die|^Das|^Der/


2.
checkItem () {
      let a = ''
      // A COMPLETER
      // ici vous fabriquez un 'a' en composant les éléments de la liste listItems
      // à l'aide d'une boucle
      for (var i = 0, n = this.listItems.length; i < n; i++) {
        a += '^' + this.listItems[i] + (i === n - 1 ? '' : '|')
      }
      if (a === '') {
        // throw Error('Le string de RE est vide')
        return
      }
      let re = new RegExp(a)
      if (re.test(this.newItem)) {
        this.propValue = this.newItem
        this.goodItems.push(this.newItem)
      } else {
        this.propValue = ''
        this.badItems.push(this.newItem)
      }
      this.newItem = ''
    }



import Vue from 'vue'
import Router from 'vue-router'
import MyRE from '@/components/MyRE'
import MyRE2 from '@/components/MyRe2'
import TestRE from '@/components/TestRE'

Vue.use(Router)

export default new Router({
  routes: [
    {
      path: '/re',
      name: 'RegEx',
      component: MyRE
    },
    {
      path: '/testre',
      name: 'TestRegEx',
      component: TestRE
    },
    {
      path: '/re2',
      name: 'RegEx2',
      component: MyRE2
    }
  ]
})
