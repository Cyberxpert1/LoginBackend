# LoginBackendcode for under development 
Javascript Based auth otp security
<form id="loginForm" class="form" @submit="loginCustomer" method="post" v-if="!opt_form">
                            <div class="form-group">
                                <label for="username">E-mail or Phone No.<span class="required">*</span></label><br>
                                <input type="text" v-model="uname"  class="form-control" >
                            </div>
                            <div class="form-group">
                                <label for="password">Password<span class="required">*</span></label><br>
                                <input type="password" v-model="password" class="form-control" >
                                <label for="lost-password" class="lost-password"><i class="fa fa-lock" aria-hidden="true"></i><a href="#" data-toggle="modal" data-target="#forgotpwmodal" data-dismiss="modal">Forgot Password</a></label>
                            </div>
                            <div class="form-group">
                                <input type="submit" name="submit" class="btn login-btn btn-block" value="LOG IN">
                             </div>
                             <div class="form-group">
                                <label for="remember-me"><span><input name="remember-me" type="checkbox"/></span><span class="remember-me">Remember me</span></label>
                                <label for="new-account" class="new-account">New to Iris Florist?<a href="#" data-toggle="modal" data-target="#signupmodal" data-dismiss="modal">Create an account</a></label>
                                
                            </div>
                             <div class="division">
                                    <div class="line l"></div>
                                      <span>OR LOGIN WITH</span>
                                    <div class="line r"></div>
                             </div>
                </form>
                
                <div class="opt_form" id="loginOtp" v-if="opt_form">
                    <p><strong>OTP sent to your registered phone number</strong></p>
                    <div class="d-flex">
                        <input type="text" pattern="\d*" maxlength="1" v-on:keyup="nextTabIndex()" class="form-control mr-2" value="" id="otp1" style="width: 60px;" />
                        <input type="text" pattern="\d*" maxlength="1" v-on:keyup="nextTabIndex()" class="form-control mr-2" value="" id="otp2" style="width: 60px;" />
                        <input type="text" pattern="\d*" maxlength="1" v-on:keyup="nextTabIndex()" class="form-control mr-2" value="" id="otp3"  style="width: 60px;"/>
                        <input type="text" pattern="\d*" maxlength="1" v-on:keyup="nextTabIndex()" class="form-control" value="" id="otp4" style="width: 60px;" />
                    </div>
                    
                    <div class="opt-buttons">
                        <button type="button" class="btn login-btn" v-on:click="verifyOtp(token,id)">Verify</button>
                    </div>
                </div>                
              </div>
