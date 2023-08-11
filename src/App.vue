<template>
  <div id="defaultRTE">
      <ejs-richtexteditor id="default" :toolbarSettings="toolbarSettings" :formatPainterSettings="formatPainterSettings">
        <h1>The Power of Format Painter in Rich Text Editing</h1>
        <p>Are you tired of manually reformatting text in your documents? Look no further than the Format Painter, a remarkable feature embedded within Rich Text Editors. This tool empowers users to effortlessly replicate formatting from one text section to another, saving valuable time and effort.</p>

        <h2>How to Use the Format Painter</h2>
        <p>To harness the potential of the Format Painter within a rich text editor, follow these simple steps:</p>
        <ol>
        <li>Highlight the text whose formatting you want to replicate.</li>
        <li>Locate and click on the Format Painter button, often represented by a paintbrush icon, found in the toolbar.</li>
        <li>Observe as your cursor transforms into a paintbrush icon, indicating the Format Painter's activation.</li>
        <li>Drag the cursor over the target text where you intend to apply the copied formatting.</li>
        <li>Release the mouse button to seamlessly transfer the chosen format to the designated text.</li>
        </ol>

        <h2>Enhance Your Efficiency</h2>
        <p>The Format Painter is a game-changer when dealing with the challenge of formatting extensive documents. This invaluable tool allows you to swiftly duplicate and apply formatting across multiple sections, eliminating the need for tedious manual adjustments.</p>
        <p>If you find yourself working with text regularly, whether you're a writer, an editor, or a content creator, the Format Painter will undoubtedly boost your productivity. Say goodbye to repetitive formatting tasks and hello to a more streamlined and efficient editing process.</p>

        <p>Experience the convenience of the Format Painter today and revolutionize the way you approach text formatting!</p>

        <p><em>Don't let formatting slow you down. Try the Format Painter and take control of your text editing experience.</em></p>
      </ejs-richtexteditor>
  </div>
</template>

<script>
  import { RichTextEditorComponent, Toolbar, Link, Image, HtmlEditor, Table, FormatPainter } from "@syncfusion/ej2-vue-richtexteditor";

  export default {
    name: "App",
    components: {
      "ejs-richtexteditor": RichTextEditorComponent,
    },

    data() {
      return {
        toolbarSettings : {
          items: ['FormatPainter', 'Bold', 'Italic', 'Underline', 'StrikeThrough',
                    'FontName', 'FontSize', 'FontColor', 'BackgroundColor', 'SuperScript', 'SubScript', '|',
                    'Formats', 'Alignments', 'NumberFormatList', 'BulletFormatList',
                    'Outdent', 'Indent', '|', 'CreateTable', 'CreateLink', 'Image', '|', 'Undo', 'Redo','SourceCode', 'FullScreen'] 
                },          
         formatPainterSettings: {
            allowedFormats: 'p;h1;h2;h3;div;ul;ol;li;span;strong;em;code;',
            deniedFormats: 'h3(e-rte-block-blue-text){background-color,padding,color}[title]; li{color}; span(e-inline-text-highlight){color}[title]; strong{color}(e-rte-strong-bg);',
          },
      };
    },
    methods: {},
    provide: {
      richtexteditor: [Toolbar, Link, Image, HtmlEditor, Table, FormatPainter],
    },
  };
     
</script>
