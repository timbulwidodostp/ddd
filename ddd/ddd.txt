# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Doubly Robust DDD estimators for the group-time average treatment effects Use ddd (triplediff) With (In) R Software
install.packages("triplediff")
library("triplediff")
# Estimation Doubly Robust DDD estimators for the group-time average treatment effects Use ddd (triplediff) With (In) R Software
ddd = read.csv("https://raw.githubusercontent.com/timbulwidodostp/ddd/main/ddd/ddd.csv", sep = ";")
ddd_1 <- ddd(yname = "y", tname = "time", idname = "id", gname = "state", pname = "partition", 
xformla = ~cov1 + cov2 + cov3 + cov4, data = ddd, control_group = "nevertreated", est_method = "dr")
summary(ddd_1)

ddd_2 <-  ddd(yname = "y", tname = "time", idname = "id", gname = "state", pname = "partition", 
xformla = ~cov1 + cov2 + cov3 + cov4, data = ddd, control_group = "nevertreated", base_period = "varying", est_method = "dr")
summary(ddd_2)

# Doubly Robust DDD estimators for the group-time average treatment effects Use ddd (triplediff) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished