#��ҵ�ʼ�
1. import��bind
import ����ĳ�������ĳ�������import * from './**'�������Щ�����Ǹ�./����������һ��js·����ֻ˵��../�ǵ��ϲ�Ŀ¼��Ȼ�������Բ��ӵ������jsx�ļ�������ļ���ͬһĿ¼�£�����Ҳ�ǿ�����..��û�پ��᣻
bind ��ʽ����?bind(this)���¼����������İ�Ҫ���ʵ���ϣ��е���bind(this,arg1,agr2..)����˵�����ĺ��ٳ��֣�this��ߵ�arg����ǰ���¼����������ҵĲ�����
2. this.props
�ĵ���˵
>React ����һ���ǳ����õ�ģʽ���Ƕ������һ�����������⹫��һ���򵥵����ԣ�Props����ʵ�ֹ��ܣ����ڲ�ϸ�ڿ����зǳ����ӵ�ʵ�֡�

     ͨ�����ھ�̬�����ϣ��ø�Ԫ���������Ͻo��Ԫ����Ԫ���Ȳ�����ͨ��this.props ȡ��ԓֵ������ͨ��?props?���Դ��ݣ��ڸ���������������?props��Ȼ��������Ϳ���ͨ��props
?���ʵ�����������ݣ������������ʹ���˸��������ͨ�ŵ�������

   ������ʹ��?[JSX չ������](http://reactjs.cn/react/docs/jsx-spread-zh-CN.html)?���ϲ����е� props ������ֵ��

   ֱ���������ʹ��key/value����ʽ��ָ������
   <pre><code>React.render(??
????<HelloWorld?name="Jack"/>,??
????document.getElementById('container')??
    );??</code></pre>

   <pre><code>
   var?HelloWorld?=?React.createClass({??
????render:?function()?{??
????????return?(??
????????????<div>Hello,?{this.props.name}</div>??
????????);??
????}??
    });??//ͨ��this.props.name�Ϳ��Ի�ȡname����ֵ��
    </code></pre>
3. this.states
React �����������һ��״̬����State Machines����ͨ�����û��Ľ�����ʵ�ֲ�ͬ״̬��Ȼ����Ⱦ UI�����û���������ݱ���һ�¡�React �ֻ���������� state��Ȼ������µ� state ������Ⱦ�û����棨��Ҫ���� DOM����
��ʼ��state �����������Ĺ��캯�����һ�£�������getInitialState�������ú���ֻ�����װ��ǰ����һ�Σ���

4. this.Setstate
����?setState(data, callback)�ǳ��õ�֪ͨ React ���ݱ仯�ķ��������������ϲ���merge��?data��?this.state����������Ⱦ�������Ⱦ��ɺ󣬵��ÿ�ѡ��?callback
?�ص����󲿷�����²���Ҫ�ṩ?callback����Ϊ React �Ḻ��ѽ�����µ�����״̬��
https://facebook.github.io/react/docs/interactivity-and-dynamic-uis-zh-CN.html

5. jsx
JSX д��һ�����ӣ�
<pre><code><--!a href="http://facebook.github.io/react/"-->Hello!</a></code></pre>
�� JS ������д�ͳ������ˣ�
<code>React.createElement('a', {href: 'http://facebook.github.io/react/'}, 'Hello!')</code>
���Ҫ��jsx�����Js����ʽ���߼�����ֵ���Ƚϣ���������λ���ַ�������Ҫ��{}��
jsx��û���޸�js���壬�ٷ�����jsx(���Լ������֪�ذ������Ե���״�ṹ�﷨)��
���ⲿ�����ݲ��ǲ�̫ס��׼���õ�ʱ���ٷ���

6. render
reactDom.render()
<code>render(ReactElement,Ԫ��
 DomElement,Ҫ��Ԫ���滻������
 [�ص�����]������ǿ�ѡ�ģ����ѡ���ˣ���ô����Ԫ�ر���Ⱦ��ʼִ��
 )
</code>
react.render
��ʹ��render����ʱ������ȷ��ֻ����һ���ڵ�(�ڵ��ڿɰ���������Ŀ�ӽڵ�)�����Ҵ���������ʹ��()���Ž����ؽ����ס���ҵ�ʱ��demo�︴�ƹ����ӣ�render�������ǩ����ȷʵ�ᱨ������
û�ҵ������˵�����о����Ǻ�������Ҫ�з���ֵ������һ�������������
>�������Ҫ��Ⱦ�κζ��������Խ�����ֵ����Ϊnull����false. �����������Reactʵ�ʻ���Ⱦһ��<noscript>��ǩ��Ȼ����ִ��diff�㷨ʱ�ᱻ�õ���

7.webpack
   ![��һ�Ź�������������ͼ](http://cdn1.infoqstatic.com/statics_s2_20160405-  0343u1/resource/articles/react-and-webpack/zh/resources/0602005.jpg)
����demo�root.jsx�о�������c�������һ��.h�ļ���main.js��һ������ļ���������������ϣ�Ȼ��bundle.js�����������Ķ���ģ�黹����ڶ�����ߣ�index.html�Ϳ���ֱ��������ű����Լ������Ԫ���ˡ�����webpack��Ҫ���õ��ļ��ҿ�������õĻ����ǻ�������ϸ㣬���о��ǲ�̫������ô��webpack���һ�����õ�react����Ŀ����

#####�����Ķ�
react�������
<code>this.state = {    inputStr: ''//������״̬�Ա㶯̬��ȡinput���ֵ}</code>
<code>return item.toLowerCase().indexOf(inputStr.toLowerCase()) >= 0//��������ַ����������ַ�����ΪСд���бȽϣ���������Ϊ��Сд�����������û��ƥ�������//���ƥ�����ȷʵ���ڣ���ô�ͷ���α��������������ַ�����tips</code>

������dom�������õ�document,window�Ȳ���������jsx��Ĳ������Ƕ������������еĲ�������Virtual DOM������ɲ�������JS��DOM�޸Ĳ�����ͨ������������ɲ㣬���ж�DOM�Ĳ�������������ʾ��DOM���ϣ����ǵȴ��¼�������е�DOM�޸�֮��ͨ��React�ڲ�ʵ�ֵ�diff�㷨���������Сdiff��Ȼ��������С�Ĳ��轫 diff ���õ���ʵ�� DOM �ϣ��������ڡ������������ÿ��React�����ӵ��һ���������������ڣ���DOM״̬�Ĳ��������������£����ھ����ܵļ���ҳ���ػ棬��׷����õ����ܡ�