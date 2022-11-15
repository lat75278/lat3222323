package com.sun.content.server.billing.external; 
 
import com.sun.content.server.billing.BillingException; 
import com.sun.content.server.billing.BillingInfo; 
import com.sun.content.server.billing.BillingManager; 
import com.sun.content.server.log.BillingManagerKeys; 
import com.sun.content.server.log.LogCategory; 
 
/** 
 * This is a sample implementation of the Billing API. 
 */ 
public class CDSBillingManager implements BillingManager 
{ 
  // These flags can be used to simulate responses from the billing 
  //integration. 
  public static final int SUCCESS = 0; 
  public static final int EXCEPTION = 1; 
  public static final int BILLING_EXCEPTION = 2; 
  public static final int UNAUTHORIZED = 3; 
  public static final int NULL = 4; 
 
  // by default everything will pass through fine 
  // but you can change these at runtime. 
  public static int AUTHORIZE_RESPONSE = SUCCESS; 
  public static int GET_BILLING_INFO_RESPONSE = SUCCESS; 
  public static int GET_BILLING_INFOS_RESPONSE = SUCCESS; 
  public static int CONFIRM_RESPONSE = SUCCESS; 
  public static int DELETE_RESPONSE = SUCCESS; 
  public static int REFUND_RESPONSE = SUCCESS; 
  public static int REVERSE_RESPONSE = SUCCESS; 
  public static int SUBSCRIBE_RESPONSE = SUCCESS; 
  public static int UNSUBSCRIBE_RESPONSE = SUCCESS; 
  public static int CHECK_SUBSCRIPTION_RESPONSE = SUCCESS; 
 
  /** 
   * This is used to log debug, warning, and error messages to the 
   * logging system. 
   */ 
  private static final LogCategory sLog = 
    LogCategory.getLog("BillingManager"); 
 
  /** 
   * see BillingManager#getBillingInfo(BillingInfo) 
   */ 
  public BillingInfo getBillingInfo(BillingInfo inBillingInfo) 
         throws BillingException 
  { 
    if (GET_BILLING_INFO_RESPONSE == NULL) 
      return null; 
 
    if (GET_BILLING_INFO_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Developer Null Pointer"); 
 
    if (GET_BILLING_INFO_RESPONSE == BILLING_EXCEPTION) 
      throw new BillingException("Developer Billing Exception"); 
 
    // Set IsAuthorizeNeeded flag 
    inBillingInfo.setAuthorizeNeeded(true); 
    return inBillingInfo; 
  } 
 
  /** 
   * see BillingManager#getBillingInfos(BillingInfo[]) 
   */ 
  public BillingInfo[]  
    getBillingInfos(BillingInfo[] inBillingInfos)  
    throws BillingException 
  { 
      for (int index = 0; index < inBillingInfos.length; index++) 
    { 
      // Set IsAuthorizeNeeded flag 
      inBillingInfos[index].setAuthorizeNeeded(true); 
    } 
 
    if (GET_BILLING_INFOS_RESPONSE == NULL) 
      return null; 
 
    if (GET_BILLING_INFOS_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Testing Null Pointer"); 
 
    if (GET_BILLING_INFOS_RESPONSE == BILLING_EXCEPTION) 
      throw new BillingException("Testing Billing Exception"); 
 
    return inBillingInfos; 
  } 
 
  /** 
   * see.BillingManager#authorize(BillingInfo, boolean[]) 
   */ 
  public BillingInfo authorize(BillingInfo inBillingInfo,  
         boolean[] inNeedToAuthorizeBillingModel) 
         throws BillingException 
  { 
    if (AUTHORIZE_RESPONSE == NULL) 
      return null; 
 
    if (AUTHORIZE_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Testing Null Pointer"); 
 
    if (AUTHORIZE_RESPONSE == BILLING_EXCEPTION) 
     throw new BillingException("Testing Billing Exception"); 
 
    if (AUTHORIZE_RESPONSE == UNAUTHORIZED) 
    { 
      inBillingInfo.setOk(false); 
      inBillingInfo.setReplyMessage("You are not authorized"); 
      return inBillingInfo; 
    } 
 
// Set IsOk and IsConfirmNeeded flags 
    inBillingInfo.setConfirmNeeded(true); 
    inBillingInfo.setOk(true); 
 
    return inBillingInfo; 
  } 
 
  /** 
   * seeBillingManager#confirm(BillingInfo) 
   */ 
  public void confirm(BillingInfo inBillingInfo) 
      throws BillingException 
  { 
    if (CONFIRM_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Developer Null Pointer"); 
 
    if (CONFIRM_RESPONSE == BILLING_EXCEPTION) 
      throw new BillingException("Developer Billing Exception"); 
  } 
 
  /** 
   * see BillingManager#reverse(BillingInfo) 
   */ 
  public void reverse(BillingInfo inBillingInfo) 
      throws BillingException 
  { 
    if (REVERSE_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Developer Null Pointer"); 
 
    if (REVERSE_RESPONSE == BILLING_EXCEPTION) 
      throw new BillingException("Developer Billing Exception"); 
  } 
 
  /** 
   * see BillingManager#refund(BillingInfo) 
   */ 
  public void refund(BillingInfo inBillingInfo) 
      throws BillingException 
  { 
    if (REFUND_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Developer Null Pointer"); 
 
    if (REFUND_RESPONSE == BILLING_EXCEPTION) 
      throw new BillingException("Developer Billing Exception"); 
  } 
 
  /** 
   * seeBillingManager#subscribe(BillingInfo) 
   */ 
  public void subscribe(BillingInfo inBillingInfo) 
      throws BillingException 
  { 
    if (SUBSCRIBE_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Developer Null Pointer"); 
 
    if (SUBSCRIBE_RESPONSE == BILLING_EXCEPTION) 
       throw new BillingException("Developer Billing Exception"); 
  } 
 
  /** 
   * see BillingManager#unsubscribe(BillingInfo) 
   */ 
  public void unsubscribe(BillingInfo inBillingInfo) 
      throws BillingException 
  { 
    if (UNSUBSCRIBE_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Developer Null Pointer"); 
 
    if (UNSUBSCRIBE_RESPONSE == BILLING_EXCEPTION) 
      throw new BillingException("Developer Billing Exception"); 
  } 
 
  /** 
   * see BillingManager#checkSubscription(BillingInfo) 
   */ 
  public BillingInfo checkSubscription(BillingInfo inBillingInfo) 
      throws BillingException 
  { 
    if (CHECK_SUBSCRIPTION_RESPONSE == NULL) 
      return null; 
 
    if (CHECK_SUBSCRIPTION_RESPONSE == EXCEPTION) 
      throw new NullPointerException("Developer Null Pointer"); 
 
    if (CHECK_SUBSCRIPTION_RESPONSE == BILLING_EXCEPTION) 
      throw new BillingException("Developer Billing Exception"); 
 
    inBillingInfo.setSubscriptionTerminated(false); 
 
    return inBillingInfo; 
  } 
 
  /** 
   * see BillingManager#contentDelete(BillingInfo) 
   */ 
  public void contentDelete(BillingInfo inBillingInfo) 
      throws BillingException 
  { 
    if (DELETE_RESPONSE == EXCEPTION) 
     throw new NullPointerException("Developer Null Pointer"); 
 
    if (DELETE_RESPONSE == BILLING_EXCEPTION) 
     throw new BillingException("Developer Billing Exception"); 
  } 
} 
