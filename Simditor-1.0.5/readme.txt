Simditor ���Ŷ�Э������ Tower ʹ�õĸ��ı��༭����



��ȴ�ͳ�ı༭�������ص��ǣ�

    ���ܾ��򣬼��ؿ���

    �����ʽ���ı�׼ HTML

    ÿһ�����ܶ��зǳ������ʹ������

    ���ݵ��������IE10+��Chrome��Firefox��Safari��



��һ�������ز�����

���������ز���ѹ���°�� Simditor �ļ���Ȼ����ҳ����������Щ�ļ���

1
2
3
4
5
6
<link rel="stylesheet" type="text/css" href="[style path]/font-awesome.css" />
<link rel="stylesheet" type="text/css" href="[style path]/simditor.css" />
<script type="text/javascript" src="[script path]/jquery.min.js"></script>
<script type="text/javascript" src="[script path]/module.js">
</script><script type="text/javascript" src="[script path]/uploader.js">
</script><script type="text/javascript" src="[script path]/simditor.js"></script>
���У�

Simditor���� jQuery ������jquery.js �Ǳ���ģ�

font-awesome.css ��һ��ͼƬ���� icon �⣬Simditor �����������幤�����İ�ť��ʽ��Ϊ���� icon �ܹ�������ʾ����Ҫ�� font �ļ���fontawesome-webfont.xxx���ŵ���ȷ��·���../fonts/������� font-awsome.css ���� styles �ļ��У���ô��Ӧ�ð� font �ļ����ڸ� styles ͬ���� fonts �ļ��У������⣬������Զ��幤������ť����ʽ�Ϳ��Բ������� font-awesome.css��

module.js �ǲʳ��ڲ�ʹ�õ� CoffeeScript ��������࣬Simditor ��������࿪����

uploader.js ��һ���� UI �޹ص��ϴ��߼�����������Ŀ����Ҫ�ϴ���������ô���Բ���������ļ���

���������Ҫ���õĽű��ļ�̫�࣬������ simditor-all.js�����������module.js uploader.js �� simditor.js���滻��

1
2
3
4
<link rel="stylesheet" type="text/css" href="[style path]/font-awesome.css" /> 
<link rel="stylesheet" type="text/css" href="[style path]/simditor.css" /> 
<script type="text/javascript" src="[script path]/jquery-2.1.0.js">
</script> <script type="text/javascript" src="[script path]/simditor-all.js"></script>


�ڶ�������ʼ������

��ʹ�� Simditor �� HTML ҳ����Ӧ����һ����Ӧ�� textarea �ı������磺

1
<textarea id="editor" placeholder="������������" autofocus></textarea>
������Ҫ�����ҳ��Ľű����ʼ�� Simditor��

var editor = new Simditor({   textarea: $('#editor') });

textarea �ǳ�ʼ�� Simditor �ı���ѡ����Խ��� jQuery Object��HTML Element ���� Selector String�����⣬Simditor ��֧����Щ��ѡ option��

placeholder��Ĭ��ֵ��''���༭���� placeholder�����Ϊ�� Simditor ��ȡ textarea �� placeholder ���ԣ�

toolbar ��Ĭ��ֵ��true���Ƿ���ʾ��������ť��

toolbarFloat ��Ĭ��ֵ��true���Ƿ��ù�������ť��ҳ������Ĺ�����ʼ�տɼ���

toolbarHidden ��Ĭ��ֵ��false���Ƿ����ع����������غ� toolbarFloat ��ʧЧ��

defaultImage��Ĭ��ֵ��'images/image.png'���༭���������ͼƬʱʹ�õ�Ĭ��ͼƬ��

tabIndent��Ĭ��ֵ��true���Ƿ��ڱ༭����ʹ�� tab ����������

params��Ĭ��ֵ��{}����ֵ�ԣ��ڱ༭�������� hidden �ֶΣ�input:hidden����ͨ���������� form ����Ĭ�ϲ�����

upload��Ĭ��ֵ��false��false ���߼�ֵ�ԣ��༭���ϴ�����ͼƬ�����ã����õ������� url �� params��

pasteImage��Ĭ��ֵ��false���Ƿ�����ճ���ϴ�ͼƬ������ upload ѡ���֧�� Firefox �� Chrome �������

����ϸ������˵�����Բο� Simditor �������ĵ����������֮��ˢ��ҳ�棬Simditor Ӧ�þͿ�����ȷ�����ˡ�



����Զ�����ʽ�ͽ���

ÿ����Ŀ���в�ͬ����Ʒ�񣬴����ʱ��������Ҫ�޸� Simditor ����ʽ����������ʽ����Ŀ�ķ�������

simditor.css ��ͨ�� Sass �Զ����ɵĴ��룬�����Ƽ�����޸� simditor.scss��Ȼ������������css���롣

.editor-style ѡ����������ʽ���� Simditor ��� HTML �������Ű���ʽ����ҿ��Ը����Լ���Ŀ��������е��������⣬�������ʹ�� font-awesome.css ��ʵ�ֹ�������ť�� icon�����Խ� font-awesome.css ȥ����Ȼ������ .toolbar-item-[button name] ѡ������Զ��尴ť��ʽ��