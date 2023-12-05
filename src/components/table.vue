<template>
	<div class="p-4">
    <table class="min-w-full bg-white">
      <thead class="text-white bg-sky-600 ">
        <tr>
          <th class="py-3 px-4 text-left uppercase font-semibold text-sm">Nome</th>
          <th class="py-3 px-4 text-left uppercase font-semibold text-sm">Cargo</th>
          <th class="py-3 px-4 text-left uppercase font-semibold text-sm">Cidade</th>
          <th class="py-3 px-4 text-left uppercase font-semibold text-sm">Idade</th>
          <th class="py-3 px-4 text-left uppercase font-semibold text-sm">Data de Início</th>
          <th class="w-10 py-3 px-4 text-left uppercase font-semibold text-sm">Salário</th>
        </tr>
      </thead>
      <tbody >
        <tr class="bg-sky-200">
          <td class="py-3 px-4 text-left ">Emanuel Nascente</td>
          <td class="py-3 px-4 text-left ">Desenvolvedor Júnior</td>
          <td class="py-3 px-4 text-left ">Porto Alegre</td>
          <td class="py-3 px-4 text-left ">32</td>
          <td class="py-3 px-4 text-left ">01/01/2023</td>
          <td class=" py-3 px-4 text-left ">$</td>
        </tr>
      </tbody>
    </table>
  </div>

</template>

<script>
export default {
	name: "Table",
};
</script>
