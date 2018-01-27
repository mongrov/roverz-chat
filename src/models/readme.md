# Models package

## naming schema 
   * entity should be named in lower case (example, User -> user) and singular
   * entity manager should be in upper case (example user manager -> UserManager)

## Todo
  * consistent naming
  * remove elix/yap from everywhere
  * in settings add a button to clear cache and wire it  
  * test cases not only to call the method, they should verify the result - otherwise it doesnt' make sense
     * remove the console.log
     * add automation to verify results of each operation
  * User 
     * statusConnection to be removed
     * avatar to be moved out - as its tied to module config
     * active - why do we want this ?
     * UserManager methods - updateStatus & updateFullUserData - should support bulk instead of individual
  * Group
     * avatar to be moved outside as well
     * GroupManager - updateNoMoreMessages - can it be a candidate for Group setter 
     * findRootMessage - shall we cache it in datastructure, so after we compute, we need not again
     * findMissingMessages - why do we check likes ?
     * GroupManager - addAll - group type should not be determined within db, should be outside this module
  * Message
     * original - should be removed
  * RemoteFile
     * if just key is coming in, don't add or delete from cache?
  * index
     * all three methods should go under groups
     * db management wrappers should be removed, should be moved to corresponding apps
     * schema.js and migrations should go under app / atleast part of it