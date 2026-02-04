# Nonlinear_nets_code_v1
Current version of the code which happens to give the opposite results
Please note that the controllability results are solely based on the first two code blocks, the blocks after I just use for visualization and testing, so they can be ignored for now. We currently use a asymmetric 5 node network as is shown in the first code block. Also I have found that when I change the coupling term, the results are actually correct, however that changes the equation so we do not want that i think. The other coupling terms are also shown as a comment in this part:     
        #coupling_x = k * np.sum(a * (x[:, None] - x[None, :]), axis=1)
        #coupling_y = k * np.sum(a * (y[:, None] - y[None, :]), axis=1)
        coupling_x = k * np.sum(a * (x[None, :] - x[:, None]), axis=1)
        coupling_y = k * np.sum(a * (y[None, :] - y[:, None]), axis=1)
