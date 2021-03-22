Vue.component('js-accordion', {
template: `
<div class="js-accordion" v-cloak>
<button class="js-accordion--trigger" type="button" :class="{ '_state-open': isOpened }" @click="accordionToggle()">
    <slot name="title"></slot>
</button>
<div class="js-accordion--target" :class="{ '_state-open': isOpened }" v-if="isOpened">
    <slot name="body"></slot>
</div>
</div>
`,

data() {
return {
isOpened: false
};
},
methods: {
accordionToggle: function(){
this.isOpened = !this.isOpened;
}
}
});
