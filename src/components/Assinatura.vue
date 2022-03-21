<template>
<div>
<div id="assinatura" style="border-style: outset; background-color: none;  max-width: 550px; padding: 20px; text-decoration: none; color: #2c3e50; font-family: Avenir, Helvetica, Arial, sans-serif; text-align: justify;">
 
<table style="height: 200px; width: 500px;">
<tbody>
<tr style="height: 13px;">
<td style="width: 160.844px; height: 13px;"><a :href="site"><img :src="logo" alt="Empresa" width="132" height="132" border="0" /></a></td>
<td style="width: 323.156px; height: 13px;">

  <div>
    <h3><strong>{{nome}}</strong></h3>
    <p><em>{{funcao}}</em></p>
  </div>
<div style="line-height: 15px;">
<p><a style="text-decoration: none; color: gray;" :href="link_telephone"><img src="../assets/telephone.png" alt="Telephone" width="20" height="20" />&nbsp;&nbsp;{{telephone}}</a></p>
<p><a style="text-decoration: none; color: gray;" :href="site"><img src="../assets/world-wide-web.png" alt="Website" width="20" height="20" />&nbsp;&nbsp;{{site}}</a></p>
<p><a style="text-decoration: none; color: gray;" :href="link_email"><img src="../assets/letter.png" alt="Email" width="20" height="20" />&nbsp;&nbsp;{{email}}</a></p>
<p><a style="text-decoration: none; color: gray;" :href="link_endereco"><img src="../assets/placeholder.png" alt="Endereço" width="20" height="20" />&nbsp;&nbsp;{{endereco}}</a></p>

<p><a :href="facebook"><img class="marging-right:10px;" src="../assets/facebook.png" alt="Facebook" width="20" height="20" data-filename="facebook.png" /></a>&ensp;&ensp;

<a :href="linkedin"><img src="../assets/linkedin.png" alt="LinkedIn" width="20" height="20" data-filename="linkedin.png" /></a>&ensp;&ensp;

<a :href="instagram"><img src="../assets/instagram.png" alt="Instagram" width="20" height="20" data-filename="instagram.png" /></a>&ensp;&ensp;

<a :href="youtube"><img src="../assets/youtube.png" alt="Youtube" width="20" height="20" data-filename="youtube.png" /></a>&ensp;&ensp;
</p>
</div>
</td>
</tr>
</tbody>
</table>
</div>
 <!-- <v-btn
      color="success"
@click="copiar"
    >
      COPIAR
    </v-btn> -->
</div>
</template>
<script>
export default {
  name: "Assinatura",
  components: {},
  props: {
  nome: String,
  funcao: String,
  logo: String,
  site:String,
  telephone:String,
  link_telephone:String,
  email:String,
  link_email:String,
  endereco: String,
  link_endereco: String,
  facebook:String,
  linkedin: String,
  instagram: String,
  youtube:String

},
  data() {},
  methods:{
     copiar() {
        let assinaturaCopiada = document.getElementById("assinatura");
        var content =assinaturaCopiada.innerHTML;
      //  const clone = assinaturaCopiada.cloneNode(true);
       navigator.clipboard.writeText(content)
        alert("O texto é: " + content);
    }
  }
};
</script>