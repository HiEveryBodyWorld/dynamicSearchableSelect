# dynamicSearchableSelect
具有查询框的 下拉列表，点击一个option 发送ajax请求 接口，将结果展示到第二个下拉列表



 <div class="row cl">
            <label class="form-label col-xs-4 col-sm-2"><span class="c-red">*</span>test名称：</label>
            <div class="formControls col-xs-8 col-sm-9" style="z-index: 200">
                <select id="bussinessID" name="bussinessID">
                    <option selected="selected" value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                    <option value="4">4</option>
                    <option value="5">5</option>

                </select>
            </div>
        </div>
        <div class="row cl">
            <label class="form-label col-xs-4 col-sm-2"><span class="c-red">*</span>test负责人：</label>
            <div class="formControls col-xs-8 col-sm-9" style="z-index: 200">
                <select id="chargePersonsID" name="chargePersonsID" >

                </select>
            </div>
        </div>


使用方法是
<script type="text/javascript">

    $(function(){

        $('#bussinessID').searchableSelectSendPost({
            'url':'http://localhost:8081/sys/commucate/getchargepersons',
            'targetID':'chargePersonsID',
            'returnField':['contact','contact2']
        });
    });

</script>

bussinessID表示的是第一个select的id值





options:
url:表示的是单击option的时候请求接口的地址
targetID；表示的是select的id的值，这个值接受接口返回的数据，将数据已option的形式拼接到select上
returnField：表示的是接口中哪些字段要显示到select下边



