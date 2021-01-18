<script>
	import * as monaco from "monaco-editor";
	import { onMount } from "svelte"
	// If you need to override the default options, you can set the override
	// const options = {};
	// new Spreadsheet('#x-spreadsheet-demo', options);

	let editorDiv, editor;

	onMount(() => {
		editor = monaco.editor.create(editorDiv, {
			value: [
				'function x() {',
				'\tconsole.log("Hello world!");',
				'}'
			].join('\n'),
			language: 'javascript'
		});
		//console.log(editor);
		//editor.onDidChangeModelContent(changes => {
			//console.log(editor.getValue());
			//console.log(changes)
		//})
	});

	
	
	//export let name;
</script>

<div style="height:100%;width:100%" bind:this={editorDiv}/>