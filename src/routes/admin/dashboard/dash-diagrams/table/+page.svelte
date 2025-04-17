<script>
    import { Table, TableBody, TableBodyCell, TableBodyRow, TableHead, TableHeadCell } from "flowbite-svelte";
    let items = [
      { id: 1, maker: "Toyota", type: "ABC", make: 2017 },
      { id: 2, maker: "Ford", type: "CDE", make: 2018 },
      { id: 3, maker: "Volvo", type: "FGH", make: 2019 },
      { id: 4, maker: "Saab", type: "IJK", make: 2020 }
    ];
</script>
  
<Table hoverable={true} >
  <TableHead>
    <TableHeadCell>ID</TableHeadCell>
    <TableHeadCell>Maker</TableHeadCell>
    <TableHeadCell>Type</TableHeadCell>
    <TableHeadCell>Make</TableHeadCell>
    <TableHeadCell>
      <span class="sr-only">Buy</span>
    </TableHeadCell>
  </TableHead>
  <TableBody>
    {#each items as item}
      <TableBodyRow>
        <TableBodyCell>{item.id}</TableBodyCell>
        <TableBodyCell>{item.maker}</TableBodyCell>
        <TableBodyCell>{item.type}</TableBodyCell>
        <TableBodyCell>{item.make}</TableBodyCell>
        <TableBodyCell>
          <a href="/tables" class="text-primary-600 dark:text-primary-500 font-medium hover:underline">Buy</a>
        </TableBodyCell>
      </TableBodyRow>
    {/each}
  </TableBody>
</Table>