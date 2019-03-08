<template>
    <div>
        <h1>Editor</h1>
        <textarea id="textarea-tinymce" ref="textarea-tinymce"></textarea>
    </div>
</template>


<script>
    import tinymce from 'tinymce'

    // A theme is also required
    import esMX from '@/static/tinymce/langs/es_MX.js';
    import '@/static/tinymce/themes/silver/theme.min.js';

    import '@/static/tinymce/skins/ui/oxide/skin.min.css';
    
    import '@/static/tinymce/plugins/paste/plugin.min.js';
    import '@/static/tinymce/plugins/link/plugin.min.js';
    import '@/static/tinymce/plugins/autoresize/plugin.min.js';
    import '@/static/tinymce/plugins/pagebreak/plugin.min.js';
    import '@/static/tinymce/plugins/preview/plugin.min.js';
    import '@/static/tinymce/plugins/print/plugin.min.js';
    import '@/static/tinymce/plugins/table/plugin.min.js';


    export default {
        created(){
            tinymce.addI18n('es_MX', esMX)
            
            tinymce.init({
                selector: 'textarea#textarea-tinymce',
                language: 'es_MX',
                plugins: ['paste', 'table', 'print', 'link', 'autoresize', 'pagebreak', 'preview']
            });
        }
        
    }
</script>
