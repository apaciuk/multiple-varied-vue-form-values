  <div class="mx-auto" style="width: 80px;">
     <b-form-input type="color" size="lg" v-model="value1" ref="value1" :value="value1" @input="setbgColor()" id="colorone" ></b-form-input>
     <b-form-input type="color" size="lg" v-model="value2" ref="value2" :value="value2" @input="setbgColor()" id="colortwo" ></b-form-input>
</div>
        <b-form-input
        id="name"
        size="lg"
        type="text"
        class="search-bar"
        placeholder="Name Your Swatch"
        v-model="value3"
        ref="value3"
        :value="value3"
        @keypress="publishSwatch"
        >
        </b-form-input>
        
  export default {      
  props:
 ['value'],
 methods: {
 useValues() {
  this.$emit('input', {
      value1: +this.$refs.value1.value,
      value2: +this.$refs.value2.value,
      value3: +this.$refs.value3.value,
 });
 // Use with this keyword
 let gradient = `linear-gradient(to right, ${this.value1}, ${this.value2})`;
 let name = (`${this.value3}`);
 // Or:
 let color1 = this.value1;
 let color2 = this.value2;
 let name = this.value3;
 }
 }
 
 (Relevent input attributes)
 
 v-model="value1" ref="value1" :value="value1"
 v-model="value2" ref="value2" :value="value2
 v-model="value3" ref="value3" :value="value3"
