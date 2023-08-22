<script lang="ts">
    import { Table } from '@skeletonlabs/skeleton';
    import type { TableSource } from '@skeletonlabs/skeleton';
    import { tableMapperValues } from '@skeletonlabs/skeleton';

    const sourceData = [
	    { position: 1, assigment: 'Task name', worker: ['<span class="badge variant-filled">kasper</span>', 'camilla', 'Karsten', 'Tobias']},
	    { position: 2, assigment: 'Helium', worker: 4.0026},
	    { position: 3, assigment: 'Lithium', worker: 6.941},
	    { position: 4, assigment: 'Beryllium', worker: 9.0122},
	    { position: 5, assigment: 'Boron', worker: 10.811},
    ];

    const tableSimple: TableSource = {
        // A list of heading labels.
        head: ['Opgave', 'Medarbejder'],
        // The data visibly shown in your table body UI.
        body: tableMapperValues(sourceData, ['assigment', 'worker']),
        // Optional: The data returned when interactive is enabled and a row is clicked.
        meta: tableMapperValues(sourceData, ['position', 'assigment', 'worker']),
        // Optional: A list of footer labels.
       //  foot: ['Total', '', '<code class="code">5</code>']
    };

    tableMapperValues(sourceData, ['name', 'symbol', 'weight'])   
</script>
Developer menu - this is the workboard <a href="/" style="color: red;">Go back to route</a>

<Table source={tableSimple} />
