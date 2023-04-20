Modal popup
 use modal popup asp.net button click event and javascript funcation
 <script>
        function ShowPopup2() {
            debugger;
            $("#loginmodal").modal("show");
            $("#loginmodal").css('background', 'inherit');
        }
        function ShowPopup() {
            debugger;
            $("#receive").modal("show");
            $("#receive").css('background', 'inherit');
        }
    </script>
    
     <div class="modal fade bd-example-modal-lg" tabindex="-1" role="dialog" aria-labelledby="myLargeModalLabel" aria-hidden="true" id="loginmodal">
        <div class="modal-dialog modal-lg">
            <div class="modal-content">
                <div class="modal-header" style="background-color: lightgray; color: white; font-family: serif">
                    <h4 class="modal-title" style="font-family: serif">Money Transfer Confirmation</h4>
                    <button class="close" data-dismiss="modal">&times;</button>
                </div>
                <div class="modal-body">
                    <div class="row" style="border: 1px solid gray; border-bottom: none">
                        <div class="col-3" style="border-right: 1px solid">
                            <span>A/c Name</span>
                        </div>
                        <div class="col-3" style="border-right: 1px solid">
                            <span>Bank Name</span>
                        </div>
                        <div class="col-3" style="border-right: 1px solid">
                            <span>Acount No</span>
                        </div>
                        <div class="col-3">
                            <span>IFSC Code</span>
                        </div>


                    </div>
                    <div class="row" style="background-color: lightgray; height: 30px; border-left: 1px solid; border-right: 1px solid">
                        <div class="col-3">
                            <asp:Label ID="lblacname" runat="server"></asp:Label>
                        </div>
                        <div class="col-3">
                            <asp:Label ID="lblbankname" runat="server"></asp:Label>
                        </div>
                        <div class="col-3">
                            <asp:Label ID="lblacountno" runat="server"></asp:Label>
                        </div>
                        <div class="col-3">
                            <asp:Label ID="lblifsc" runat="server"></asp:Label>
                        </div>

                    </div>
                    <div class="row" style="border: 1px solid gray; border-left: 1px solid; border-right: 1px solid">
                        <div class="col-3" style="border-right: 1px solid">
                            <span>Amount</span>
                        </div>
                        <div class="col-3" style="border-right: 1px solid">
                            <span>Subcharge</span>
                        </div>
                        <div class="col-3" style="border-right: 1px solid">
                            <span>Commission</span>
                        </div>
                        <div class="col-3">
                            <span>Total Amount</span>
                        </div>


                    </div>
                    <div class="row" style="background-color: lightgray; height: 30px; border: 1px solid; border-top: none">
                        <div class="col-3">
                            <asp:Label ID="lblamount" runat="server"></asp:Label>
                        </div>
                        <div class="col-3">
                            <asp:Label ID="lblsucharge" runat="server"></asp:Label>
                        </div>
                        <div class="col-3">
                            <asp:Label ID="lblCommission" runat="server"></asp:Label>
                        </div>
                        <div class="col-3">
                            <asp:Label ID="lblTtalAmount" runat="server"></asp:Label>
                        </div>

                    </div>
                    <div class="row" style="border: 1px solid gray; border: 1px solid; border-top: none">
                        <div class="col-3" style="border-right: 1px solid">
                        </div>
                        <div class="col-3" style="border-right: 1px solid">
                        </div>
                        <div class="col-3" style="border-right: 1px solid">
                            <span>Grad Total</span>
                        </div>
                        <div class="col-3">
                            <asp:Label ID="lblgradTotal" runat="server"></asp:Label>
                        </div>


                    </div>
                </div>
                <div class="modal-footer">
                    <asp:Button CssClass="btn btn-primary" ID="btn_pay" Text="Pay" runat="server" OnClick="btn_pay_Click" />
                    <button class="btn btn-primary" data-dismiss="modal">Close</button>

                </div>
            </div>
        </div>
    </div>
    
    cs code 
      ScriptManager.RegisterStartupScript(Page, Page.GetType(), "myModal", "$('#loginmodal').modal('show');", true);
